<div align="center">
  
# Selenium Smoke Tests

*Production-ready test automation suite with comprehensive web testing scenarios*

[![GitHub stars](https://img.shields.io/github/stars/damianczer/Selenium-Smoke-Tests?style=for-the-badge&color=gold)](https://github.com/damianczer/Selenium-Smoke-Tests/stargazers)
[![GitHub watchers](https://img.shields.io/github/watchers/damianczer/Selenium-Smoke-Tests?style=for-the-badge&color=blue)](https://github.com/damianczer/Selenium-Smoke-Tests/watchers)
[![GitHub issues](https://img.shields.io/github/issues/damianczer/Selenium-Smoke-Tests?style=for-the-badge&color=red)](https://github.com/damianczer/Selenium-Smoke-Tests/issues)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=for-the-badge)](https://opensource.org/licenses/MIT)

| Technology | Purpose | Documentation |
|------------|---------|---------------|
| ![Robot Framework](https://img.shields.io/badge/Robot_Framework-000000?style=for-the-badge&logo=robotframework&logoColor=white) | Test Automation Framework | [User Guide](https://robotframework.org/robotframework/latest/RobotFrameworkUserGuide.html) |
| ![SeleniumLibrary](https://img.shields.io/badge/SeleniumLibrary-43B02A?style=for-the-badge&logo=selenium&logoColor=white) | Browser Automation Library | [Documentation](https://robotframework.org/SeleniumLibrary/SeleniumLibrary.html) |
| ![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white) | Programming Language | [Documentation](https://docs.python.org/3/) |
| ![The Internet](https://img.shields.io/badge/Test_Application-4A4A4A?style=for-the-badge&logo=googlechrome&logoColor=white) | Demo Web App for Testing | [The Internet](https://the-internet.herokuapp.com/) |
| ![Robot Syntax](https://img.shields.io/badge/Robot_Syntax-000000?style=for-the-badge&logo=robotframework&logoColor=white) | Test Data & Keyword Syntax | [Syntax Guide](https://robotframework.org/robotframework/latest/RobotFrameworkUserGuide.html#test-data-syntax) |

This project demonstrates best practices in test automation with a focus on maintainability, scalability, and CI/CD integration.



### Test Coverage
Currently implemented test suites covering **93 test scenarios**:

| Test Suite | Test Cases | Coverage |
|------------|------------|----------|
| **A/B Testing** | 5 scenarios | Variant testing, page refresh, content validation |
| **Add/Remove Elements** | 8 scenarios | DOM manipulation, performance testing |
| **Basic Auth** | 8 scenarios | HTTP authentication, security validation |
| **Checkboxes** | 8 scenarios | Form elements, state management, persistence testing |
| **Context Menu** | 8 scenarios | Mouse interactions, element properties, UI testing |
| **Dropdown** | 8 scenarios | Select elements, form validation, option management |
| **Drag and Drop** | 8 scenarios | Element manipulation, drag interactions, UI controls |
| **File Upload** | 8 scenarios | File handling, form submissions, upload validation |
| **JavaScript Alerts** | 8 scenarios | Alert dialogs, confirm dialogs, prompt dialogs |
| **Dynamic Loading** | 8 scenarios | Dynamic content loading, element visibility, AJAX testing |
| **Hovers** | 8 scenarios | Mouse hover interactions, tooltip display, UI feedback |
| **Inputs** | 8 scenarios | Number input validation, keyboard interactions, form fields |

Execution:

<img width="692" height="312" alt="image" src="https://github.com/user-attachments/assets/3586fcf9-ad17-46ca-810c-7efd01138b34" />

Raport:

<img width="913" height="890" alt="image" src="https://github.com/user-attachments/assets/af25dfc8-8fcf-4112-afc3-c300d6613a3d" />

</div>

## Quick Demo

```bash
# Clone and run in 3 commands
git clone <repository-url>
cd Automatic-Tests
pip install -r requirements.txt

# Run smoke tests (takes ~2 minutes)
run_tests.bat smoke
```
## Prerequisites

- Python 3.8 or higher
- pip (Python package manager)
- Google Chrome or Firefox browser
- Git (for cloning the repository)

## Installation

### Step 1: Create virtual environment (recommended)
```bash
# Create virtual environment
python -m venv venv

# Activate virtual environment
# On Windows:
venv\Scripts\activate
# On macOS/Linux:
source venv/bin/activate
```

### Step 2: Install dependencies
```bash
pip install -r requirements.txt
```

## Running Tests

### Quick Start (Windows)
Use the provided batch script for easy test execution:
```cmd
# Run all tests (93 test cases)
run_tests.bat

# Run only smoke tests (16 critical test cases)
run_tests.bat smoke

# Run A/B Testing tests only (5 test cases)
run_tests.bat ab_testing

# Run Add/Remove Elements tests only (8 test cases)
run_tests.bat add_remove

# Run Basic Auth tests only (8 test cases)
run_tests.bat basic_auth

# Run Checkboxes tests only (8 test cases)
run_tests.bat checkboxes

# Run Context Menu tests only (8 test cases)
run_tests.bat context_menu

# Run Dropdown tests only (8 test cases)
run_tests.bat dropdown

# Run Drag and Drop tests only (8 test cases)
run_tests.bat drag_and_drop

# Run File Upload tests only (8 test cases)
run_tests.bat file_upload

# Run JavaScript Alerts tests only (8 test cases)
run_tests.bat javascript_alerts

# Run Dynamic Loading tests only (8 test cases)
run_tests.bat dynamic_loading

# Run Hovers tests only (8 test cases)
run_tests.bat hovers

# Run Inputs tests only (8 test cases)
run_tests.bat inputs

# Run in headless mode
run_tests.bat basic_auth

# Run tests in headless mode (no browser window)
run_tests.bat headless
```

### Manual Execution

#### Run all tests:
```bash
python -m robot -d results tests/
```

#### Run specific test file:
```bash
# A/B Testing (5 test cases)
python -m robot -d results tests/ab_testing.robot

# Add/Remove Elements (8 test cases)
python -m robot -d results tests/add_remove_elements.robot

# Basic Auth (8 test cases)
python -m robot -d results tests/basic_auth.robot

# Checkboxes (8 test cases)
python -m robot -d results tests/checkboxes.robot

# Context Menu (8 test cases)
python -m robot -d results tests/context_menu.robot

# Dropdown (8 test cases)
python -m robot -d results tests/dropdown.robot

# Drag and Drop (8 test cases)
python -m robot -d results tests/drag_and_drop.robot

# File Upload (8 test cases)
python -m robot -d results tests/file_upload.robot

# JavaScript Alerts (8 test cases)
python -m robot -d results tests/javascript_alerts.robot

# Dynamic Loading (8 test cases)
python -m robot -d results tests/dynamic_loading.robot

# Hovers (8 test cases)
python -m robot -d results tests/hovers.robot

# Inputs (8 test cases)
python -m robot -d results tests/inputs.robot
```

#### Run tests with specific browser:
```bash
# Chrome (default)
python -m robot -v BROWSER:chrome -d results tests/

# Firefox
python -m robot -v BROWSER:firefox -d results tests/

# Headless Chrome
python -m robot -v BROWSER:chrome -v HEADLESS:True -d results tests/
```

#### Run tests with tags:
```bash
# Run only smoke tests (16 test cases)
python -m robot -i smoke -d results tests/

# Run authentication tests (Basic Auth - 8 test cases)
python -m robot -i authentication -d results tests/

# Run functionality tests (multiple test cases)
python -m robot -i functionality -d results tests/

# Run form elements tests
python -m robot -i forms -d results tests/

# Run tests excluding slow ones
python -m robot -e slow -d results tests/

# Run specific functionality tests
python -m robot -i ab_testing -d results tests/
python -m robot -i basic_auth -d results tests/
python -m robot -i checkboxes -d results tests/
python -m robot -i context_menu -d results tests/
python -m robot -i dropdown -d results tests/
python -m robot -i drag_and_drop -d results tests/
python -m robot -i file_upload -d results tests/
```

## Test Results

After running tests, results are available in the `results/` directory:
- **report.html** - High-level test report
- **log.html** - Detailed execution log
- **output.xml** - Machine-readable results

### Opening Results
```bash
# Open report in default browser (Windows)
start results/report.html

# Open detailed log
start results/log.html
```

## Configuration

### Browser Configuration
Edit `resources/variables.robot` to change default settings:
```robot
${BROWSER}               chrome        # Default browser
${HEADLESS}              False         # Run in headless mode
${IMPLICIT_WAIT}         10            # Default wait time
${WINDOW_WIDTH}          1920          # Browser window width
${WINDOW_HEIGHT}         1080          # Browser window height
```

### Test Configuration
Edit `robot.yaml` for global Robot Framework settings.

## Available Test Suites

### A/B Testing (`tests/ab_testing.robot`)
Tests the A/B Testing functionality on the-internet.herokuapp.com:
- TC001: Check A/B Testing link availability on homepage
- TC002: Navigate from homepage to A/B Testing page
- TC003: Verify A/B Testing page content
- TC004: Check A/B Testing variant display
- TC005: Test page refresh behavior

**Tags:** `smoke`, `navigation`, `content`, `functionality`, `ab_testing`, `refresh`

### Add/Remove Elements (`tests/add_remove_elements.robot`)
Tests dynamic DOM manipulation functionality:
- TC001: Check Add/Remove Elements link availability on homepage
- TC002: Navigate to Add/Remove Elements page
- TC003: Verify basic page functionality
- TC004: Add single element
- TC005: Add and remove element (full cycle)
- TC006: Add multiple elements
- TC007: Remove all elements
- TC008: Performance test with many elements

**Tags:** `smoke`, `navigation`, `content`, `functionality`, `performance`, `add_remove`

### Basic Auth (`tests/basic_auth.robot`)
Tests HTTP Basic Authentication functionality:
- TC001: Check Basic Auth link availability on homepage
- TC002: Navigate to Basic Auth page with credentials
- TC003: Verify Basic Auth success page content
- TC004: Basic Auth via homepage navigation
- TC005: Multiple Basic Auth access attempts
- TC006: Basic Auth page refresh behavior
- TC007: Basic Auth URL structure validation
- TC008: Basic Auth security headers check

**Tags:** `smoke`, `navigation`, `content`, `functionality`, `authentication`, `security`, `basic_auth`

### Checkboxes (`tests/checkboxes.robot`)
Tests form elements and checkbox state management:
- TC001: Check Checkboxes link availability on homepage
- TC002: Navigate to Checkboxes page
- TC003: Verify Checkboxes page content
- TC004: Check initial checkbox states
- TC005: Toggle first checkbox
- TC006: Toggle second checkbox
- TC007: Multiple checkbox operations
- TC008: Checkbox persistence test

**Tags:** `smoke`, `navigation`, `content`, `functionality`, `forms`, `checkboxes`

### Context Menu (`tests/context_menu.robot`)
Tests context menu interactions and mouse event handling:
- TC001: Check Context Menu link availability on homepage
- TC002: Navigate to Context Menu page
- TC003: Verify Context Menu page content
- TC004: Test right click context menu alert (element interaction)
- TC005: Test context menu element interaction
- TC006: Test context menu box properties
- TC007: Multiple context menu box interactions
- TC008: Context menu page elements verification

**Tags:** `smoke`, `navigation`, `content`, `functionality`, `interaction`, `context_menu`

### Dropdown (`tests/dropdown.robot`)
Tests dropdown/select element functionality and form interactions:
- TC001: Check Dropdown link availability on homepage
- TC002: Navigate to Dropdown page
- TC003: Verify Dropdown page content
- TC004: Verify dropdown default state
- TC005: Select Option 1 from dropdown
- TC006: Select Option 2 from dropdown
- TC007: Multiple dropdown selections
- TC008: Dropdown options verification

**Tags:** `smoke`, `navigation`, `content`, `functionality`, `forms`, `dropdown`

### Drag and Drop (`tests/drag_and_drop.robot`)
Tests drag and drop interactions and element manipulation:
- TC001: Check Drag and Drop link availability on homepage
- TC002: Navigate to Drag and Drop page
- TC003: Verify Drag and Drop page content
- TC004: Verify initial state of drag and drop elements
- TC005: Drag element from column A to column B
- TC006: Drag element from column B to column A
- TC007: Multiple drag and drop operations
- TC008: Drag and drop elements properties verification

**Tags:** `smoke`, `navigation`, `content`, `functionality`, `interaction`, `drag_and_drop`

### File Upload (`tests/file_upload.robot`)
Tests file upload functionality and form submissions:
- TC001: Check File Upload link availability on homepage
- TC002: Navigate to File Upload page
- TC003: Verify File Upload page content
- TC004: Verify file upload elements properties
- TC005: Upload text file
- TC006: Upload different file types
- TC007: Multiple file upload operations
- TC008: File upload form validation

**Tags:** `smoke`, `navigation`, `content`, `functionality`, `forms`, `file_upload`

### JavaScript Alerts (`tests/javascript_alerts.robot`)
Tests JavaScript alert dialogs, confirm dialogs, and prompt dialogs:
- TC001: Check JavaScript Alerts link availability on homepage
- TC002: Navigate to JavaScript Alerts page
- TC003: Verify JavaScript Alerts page content
- TC004: Test JavaScript Alert dialog
- TC005: Test JavaScript Confirm dialog accept
- TC006: Test JavaScript Confirm dialog dismiss
- TC007: Test JavaScript Prompt dialog
- TC008: Multiple JavaScript alerts operations

**Tags:** `smoke`, `navigation`, `content`, `functionality`, `alerts`, `javascript_alerts`

### Dynamic Loading (`tests/dynamic_loading.robot`)
Tests dynamic content loading and element visibility changes:
- TC001: Check Dynamic Loading link availability on homepage
- TC002: Navigate to Dynamic Loading page
- TC003: Verify Dynamic Loading page content
- TC004: Test dynamic loading Example 1 - hidden element
- TC005: Test dynamic loading Example 2 - rendered element
- TC006: Verify loading states Example 1
- TC007: Verify loading states Example 2
- TC008: Multiple dynamic loading operations

**Tags:** `smoke`, `navigation`, `content`, `functionality`, `ajax`, `dynamic_loading`

### Hovers (`tests/hovers.robot`)
Tests mouse hover interactions and tooltip display:
- TC001: Check Hovers link availability on homepage
- TC002: Navigate to Hovers page
- TC003: Verify Hovers page content
- TC004: Test hover on User 1
- TC005: Test hover on User 2
- TC006: Test hover on User 3
- TC007: Verify user profile links
- TC008: Multiple hover operations

**Tags:** `smoke`, `navigation`, `content`, `functionality`, `interactions`, `hovers`

### Inputs (`tests/inputs.robot`)
Tests number input fields and keyboard interactions:
- TC001: Check Inputs link availability on homepage
- TC002: Navigate to Inputs page
- TC003: Verify Inputs page content
- TC004: Test number input with valid number
- TC005: Test number input with negative number
- TC006: Test number input with zero
- TC007: Test number input increment and decrement
- TC008: Multiple input operations

**Tags:** `smoke`, `navigation`, `content`, `functionality`, `forms`, `inputs`

<div align="center">

### Author: Damian Czerwiński

</div>

<div align="center">

**Made with ❤️ for the TEST Community**

</div>
