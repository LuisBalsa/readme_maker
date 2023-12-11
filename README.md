# Readme for Code 42 School Project Summary Script
![enter image description here](https://private-user-images.githubusercontent.com/81270660/289586215-fcfca26c-3671-4fa5-9f80-d009028dcded.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTEiLCJleHAiOjE3MDIzMDkwOTAsIm5iZiI6MTcwMjMwODc5MCwicGF0aCI6Ii84MTI3MDY2MC8yODk1ODYyMTUtZmNmY2EyNmMtMzY3MS00ZmE1LTlmODAtZDAwOTAyOGRjZGVkLnBuZz9YLUFtei1BbGdvcml0aG09QVdTNC1ITUFDLVNIQTI1NiZYLUFtei1DcmVkZW50aWFsPUFLSUFJV05KWUFYNENTVkVINTNBJTJGMjAyMzEyMTElMkZ1cy1lYXN0LTElMkZzMyUyRmF3czRfcmVxdWVzdCZYLUFtei1EYXRlPTIwMjMxMjExVDE1MzMxMFomWC1BbXotRXhwaXJlcz0zMDAmWC1BbXotU2lnbmF0dXJlPTdlOWU1MjE4Y2ZhMmZmZmJkNjFjMThiZTQ1NWMyMWEwZDcyZmUzMjkzZGY5NWFmZjIxZDk1ZmUxMDFhMDc2ZmUmWC1BbXotU2lnbmVkSGVhZGVycz1ob3N0JmFjdG9yX2lkPTAma2V5X2lkPTAmcmVwb19pZD0wIn0.dt7UszpJLzxQXAjlB1c5v2FIRUqPKCFrORUxHPq-u7Q)
## Overview

This script is designed to generate a summary of C programming projects completed at Code 42 school. It extracts relevant information, such as code files, functions, and subject details, and compiles them into a structured summary. The generated summary is intended to be used as a starting point for creating a detailed README file for the project on GitHub.

## Purpose

The primary purpose of this script is to streamline the process of creating README files for Code 42 school projects. It automates the extraction of important information from code files and compiles it into a format suitable for documentation. The generated summary can be used as a foundation for creating comprehensive README files that explain the project, its requirements, and the implemented code.

## How to Use

1. **Move the Script to `/usr/local/bin`:**
   - For ease of use, consider moving the script to a directory in your system's `PATH`, such as `/usr/local/bin`. You can use the following commands:
     ```bash
     sudo cp readme_maker.sh /usr/local/bin/readme_maker
     sudo chmod +x /usr/local/bin/readme_maker
     ```

2. **Run the Script Anywhere:**
   - After moving the script to `/usr/local/bin`, you can run it from any directory without specifying the script's location.

3. **Follow Prompts:**
   - The script prompts the user for confirmation before removing existing files. Follow the prompts to proceed or cancel the process.

4. **Provide Ignore Folders (Optional):**
   - Optionally, you can provide folder names as arguments to ignore specific folders during processing. For example:
     ```bash
     readme_maker folder_to_ignore
     ```

5. **Review Output:**
   - The script processes code files (`.c`, `.h`, `.cpp`, `.hpp`, `Makefile`) in the current directory, its subdirectories and extracts relevant information.
   - If `en.subject.pdf` is present in the current directory, it is also processed.
   - The output is stored in a file named `summary.txt`.

6. **Copy to Clipboard:**
   - The script copies the content of `summary.txt` to the clipboard.
   - Paste the content into ChatGPT to receive a detailed README for the project.

7. **Customization (Optional):**
   - Modify the `regex_func` and `file_extensions` variables in the script to adapt it to other programming languages.
   - Customize the script to meet specific project requirements.

## Customization Guide

### Changing Regular Expression (`regex_func`)

- The `regex_func` variable is responsible for extracting function signatures from code files.
- Modify the regular expression to match the function signature format of the target programming language.
- Be cautious while changing the regular expression to ensure accurate function extraction.

### Adapting to Other Languages (`file_extensions`)

- The `file_extensions` array lists the file extensions to be processed (e.g., `.c`, `.h`, `.cpp`, `.hpp`, `Makefile`).
- Update the array with the relevant file extensions for the target programming language.
- Ensure that the selected file extensions cover the source code and build/configuration files of the project.

## Example Usage

```bash
readme_maker folder_to_ignore
```

This command runs the script, ignoring the specified folder during processing.

## Processing `en.subject.pdf`

- The script automatically checks if the `en.subject.pdf` file is present in the current directory.
- If the file exists, it is processed to extract relevant information for the project summary.

## Notes

- The script automatically removes redundant comments, empty lines, and specific preprocessor directives to enhance the clarity of the generated summary.
- Always review and edit the generated README to provide a detailed and accurate representation of the project.


---

**Note:** Please ensure that the required dependencies (e.g., `pdftotext`, `xclip`) are installed on your system before running the script.
