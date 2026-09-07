# GitHub Actions - UI Automation Test

A simple **UI Automation Testing** project using **Puppeteer** and **GitHub Actions** to demonstrate automated testing and CI workflow.

## 📌 Project Overview

This project demonstrates how UI tests can be automated and integrated into a **CI/CD pipeline** using GitHub Actions.

The test simulates a real user interacting with a web page and verifies that the system correctly validates user input.

### What is tested?

| Test Case | Input        | Expected Result |
| --------- | ------------ | --------------- |
| TC01      | `Siriluk`    | Pass            |
| TC02      | `123456`     | Fail            |
| TC03      | `Siriluk999` | Fail            |

The automation test opens `index.html`, enters test data, clicks the button, captures the browser alert, and verifies the actual result against the expected behavior.

## 🛠️ Tech Stack

* **JavaScript** — Test scripting
* **Puppeteer** — Browser/UI automation
* **HTML / CSS** — Test target application
* **GitHub Actions** — CI automation
* **HTMLHint** — HTML validation
* **JSHint** — JavaScript validation
* **Stylelint** — CSS validation

## 🔄 Automation Flow

```text
Code Push
    ↓
GitHub Actions
    ↓
Code Quality Check
    ├── HTMLHint
    ├── JSHint
    ├── Stylelint
    └── Regex Validation
    ↓
UI Automation Test
    ↓
Puppeteer
    ↓
Open index.html
    ↓
Enter Test Data
    ↓
Click Button
    ↓
Verify Alert Result
    ↓
PASS / FAIL
```

## 📂 Project Structure

```text
GitHubAction_AutoTest/
│
├── .github/
│   └── workflows/
│       ├── AutoCheck.yml
│       ├── AutoAlert.yml
│       ├── AutoMarge.yml
│       └── AutoPullRequest.yml
│
├── index.html       # Web page used as the test target
├── script.js        # Application logic and input validation
├── style.css        # UI styling
├── ui-test.js       # Automated UI test using Puppeteer
└── README.md        # Project documentation
```

## 🎯 Purpose

This project was created to practice and demonstrate:

* UI Automation Testing
* Test Case Design
* Positive & Negative Testing
* Input Validation Testing
* Automated Test Execution
* CI/CD with GitHub Actions
* Code Quality Checks
* Automated Pull Request workflow

## 🚀 Key Concept

The main goal is to ensure that changes to the application can be automatically validated before they are merged.

If the automated test detects an unexpected behavior, the GitHub Actions workflow will fail, helping prevent defective code from being merged.

---

**Project Type:** QA / Test Automation Portfolio
**Focus:** UI Automation + CI/CD
