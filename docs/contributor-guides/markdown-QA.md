# Contributor Quality Assurance (QA) Guide

## Introduction
This guide explains how contributors to this repository should use **Vale** and **markdownlint-cli** to ensure that all Markdown files in this repository meet high-quality standards before being pushed to the default branch.

## Linting with Vale
Vale is a tool that checks Markdown files for style and grammar issues based on a set of predefined rules. To use Vale for linting Markdown files:

### Step 1: Install Vale
Follow the [installation instructions](https://vale.sh/docs/install) to install Vale. 

The use of vale requires three components: a .vale.ini config file, a StylesPath directory (specified in the config file), and a document or directory to lint. The [Vale Config Generator](https://vale.sh/generator) can be used to create the content for the .vale.ini file, using the following configurations: Google Developer Documentation Style Guide, write-good, and MDX. 

### Step 2: Running Vale
1. Clone the repository to your local machine (if you haven’t already done so).
2. Navigate to the root of the repository.
3. In your terminal, run the following command to lint all Markdown files:
   `vale .`

### Step 3: Review the Results
Vale will output any issues it finds in the Markdown files. These may include:
- Grammar and spelling errors
- Inconsistent writing style (e.g., inconsistent use of commas, capitalization)
- Suggestions for improving readability

### Step 4: Fix the Issues
Review the suggestions or errors provided by Vale. Make the necessary changes to the Markdown files based on these recommendations. Once all issues have been resolved, you can commit the changes.

## Linting with markdownlint-cli
markdownlint-cli checks the formatting of Markdown files to ensure they follow best practices. To use markdownlint-cli:

### Step 1: Install markdownlint-cli
For more details on markdownlint-cli, refer to the [official documentation](https://github.com/igorshubovych/markdownlint-cli/tree/master?tab=readme-ov-file#usage).

Install markdownlint-cli globally by running:
   `npm install -g markdownlint-cli`

On macOS, you can install via Homebrew:
   `brew install markdownlint-cli`

### Step 2: Running markdownlint-cli
1. Navigate to the root of the repository.
2. Run the following command to check all Markdown files in the repository:
   `markdownlint .`

### Step 3: Review the Results
markdownlint-cli will output any formatting issues, such as:
- Line length exceeding the limit (typically 80 characters)
- Missing or extra spaces after headings or list items
- Incorrect use of Markdown syntax (e.g., inconsistent use of list markers)

### Step 4: Fix the Issues
Review the results and fix any Markdown formatting issues. Follow the recommendations provided by markdownlint-cli to ensure the file adheres to the repository’s formatting standards.

## Commit and Push Changes
After fixing any issues flagged by Vale and markdownlint-cli, commit your changes and push them to your feature branch. Make sure that all changes pass the linting checks before pushing them.

### Step 1: Stage Your Changes
`git add .`

### Step 2: Commit Your Changes
`git commit -m "Fix linting and formatting issues in markdown files"`

### Step 3: Push Your Changes
`git push origin <your-feature-branch>`

Replace <your-feature-branch> with the actual name of your feature branch before running the command.

Once you have pushed your changes, open a pull request to merge your feature branch into the default branch. The pull request will be reviewed, and any issues found in the markdown files will need to be addressed before it is merged.

## Conclusion
By using Vale and markdownlint-cli, you ensure that all Markdown files in this repository meet high standards for spelling, grammar, style, and formatting. Following these steps will help maintain consistent, readable, and high-quality documentation in this repository.
