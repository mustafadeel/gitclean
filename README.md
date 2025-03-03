# Installation
To use this hook:

Save the script as .git/hooks/pre-commit in your repository
Make it executable with chmod +x .git/hooks/pre-commit

The hook will automatically create the Python scanner script in .git/tools/secret_scanner.py when first run.

# Introduction
This pre-commit hook will:
- Check for staged files in your commit
- Create a Python script for scanning secrets if it doesn't exist already
- Run the scanner on all staged files
- If potential secrets are found, alert the developer and provide an option to abort

Everything runs locally on your machine!

# Supported Secrets
The Python script includes regex patterns to detect common secrets like:

AWS keys
Private keys
API keys
GitHub tokens
Password assignments
Connection strings
Auth0 Secrets
Stripe Secrets
Generic secrets
