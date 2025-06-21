Project Setup Guide

This guide provides simple steps to set up and run your project.

Requirements

   Python 3.x

    Google Chrome browser

     ChromeDriver compatible with your Chrome version

Steps to Set Up the Project

1. Create and Activate a Virtual Environment

*Run the following command to create a virtual environment:

    python -m venv venv

*Activate the virtual environment:

   On Windows:

     venv\Scripts\activate

*On macOS/Linux:

    source venv/bin/activate

2. Install Dependencies

*Run this command to install required packages:

pip install selenium pytest pytest-html pyyaml pylint pandas webdriver-manager

*Alternatively, use the requirements.txt file:

pip install -r requirements.txt

3. Set ChromeDriver Path

Update the ChromeDriver path in these files:

   1.test_workflow.py

   2.conftest.py

   3.utils/config.py

Example:

CHROME_DRIVER_PATH = "path/to/chromedriver"

4. Run the Tests

*Execute tests with the following command:

pytest --html=report.html

*This will create an HTML report named report.html.

Project Structure

project-directory/
├── test_workflow.py         # Main test file
├── conftest.py              # Pytest configuration
├── utils/
│   └── config.py           # Configuration settings
├── requirements.txt         # Dependencies
├── venv/                    # Virtual environment folder
└── other files

Tips

*Use pylint for code quality checks:

pylint your_script.py

*Save dependencies to requirements.txt:

pip freeze > requirements.txt

Troubleshooting

*Ensure ChromeDriver version matches your Chrome browser. Download the correct version from here.

*If dependency installation fails, check Python version and package documentation.

