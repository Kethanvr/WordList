# Wordlist Generator

A Python command-line utility that builds wordlist candidates from supplied target context, applies length filters, and saves the result for a permitted security assessment. It supports interactive prompts and command-line options for service type, input terms, complexity, output path, and length limits.

## Requirements

Python 3 and the packages imported by `word_list.py` are required. Install the dependencies listed in the project’s dependency file if one is added; this repository currently does not provide a pinned requirements file.

## Run

Start the interactive flow with:

    python readme.py

For command-line mode, the entry point is `word_list.py`. For example, use only a lab target you own or have explicit authorization to test:

    python word_list.py --service ssh --ip 192.0.2.10 --username test-user --output results/lab-wordlist.txt

The generator writes candidate strings to a local file. Handle generated files as sensitive data, and delete them when the authorized assessment is complete. The tool does not itself verify authorization or perform network testing.

## Responsible use

Use this tool only for systems you own or are explicitly authorized to assess. Do not use personal information to create guesses for real accounts. Follow applicable laws and the rules of the assessment environment.
