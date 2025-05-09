# **AI_UI_Validator**

**AI_UI_Validator** is a lightweight, intelligent tool designed to validate and detect visual changes in web UIs using **Selenium** and **OpenCV**. It automates browser interactions, captures baseline and altered UI screenshots, and highlights any discrepancies—making it ideal for UI regression testing in modern web development workflows.

---

## **Table of Contents**

- [Overview](#overview)
- [Features](#features)
- [Tech Stack](#tech-stack)
- [Project Structure](#project-structure)
- [Installation](#installation)
- [Usage](#usage)
- [Sample Output](#sample-output)
- [Quick Start](#quick-start-run-locally)
- [Use Case](#use-case)
- [Future Improvements](#future-improvements)
- [Author](#author)

---

## **Overview**

In web development, UI inconsistencies can sneak in unnoticed with each new deployment. **AI_UI_Validator** helps detect those changes by:

- Capturing a baseline UI screenshot.
- Performing UI interactions to simulate changes.
- Taking a new screenshot after changes.
- Using image processing (**OpenCV**) to compare both screenshots and highlight differences.

This project demonstrates an automated and visual approach to front-end regression testing.

---

## **Features**

- Automated browser control using Selenium WebDriver
- Simulated user interaction to modify UI state
- Baseline and updated UI screenshot capture
- Pixel-level comparison using OpenCV
- Visual difference output in a separate image
- User-friendly CLI logging

---

## **Tech Stack**

- **Python 3**
- **Selenium** - Automates browser actions
- **OpenCV** - Image comparison and visualization
- **NumPy** - Efficient image processing
- **Google Chrome + Chromedriver** - Target browser

---

## **Project Structure**

```text
AI_UI_Validator/
├── capture_baseline.py        # Captures the initial state of the web UI
├── capture_changed_ui.py     # Simulates user activity and captures modified UI
├── compare_ui.py             # Compares both screenshots and detects UI differences
├── saucedemo_baseline.png    # Baseline screenshot (auto-generated)
├── saucedemo_changed.png     # Changed screenshot (auto-generated)
├── ui_diff.png               # Output image showing visual differences
```

---

## **Installation**

### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/AI_UI_Validator.git
cd AI_UI_Validator
```

### 2. Install Dependencies

```bash
pip install selenium opencv-python numpy
```

### 3. Download ChromeDriver

Ensure the version matches your Chrome browser. Add it to your system PATH or specify its path explicitly in the scripts.

---

## **Usage**

### 1. Capture Baseline Screenshot

```bash
python capture_baseline.py
```

### 2. Capture Changed UI Screenshot

```bash
python capture_changed_ui.py
```

### 3. Compare Screenshots & Detect Differences

```bash
python compare_ui.py
```

After running the final step, a new image (`ui_diff.png`) will be generated highlighting visual differences in white.

---

## **Sample Output**

- `saucedemo_baseline.png`: Screenshot of the default SauceDemo homepage
- `saucedemo_changed.png`: Screenshot after adding an item to the cart
- `ui_diff.png`: Highlights UI differences between the two screenshots using pixel-level comparison

---

## **Quick Start (Run Locally)**

```bash
# Step 1: Clone the repository
git pull https://github.com/yourusername/AI_UI_Validator.git

# Step 2: Install dependencies
pip install -r requirements.txt

# Step 3: Capture baseline UI
python capture_baseline.py

# Step 4: Simulate UI change and capture updated state
python capture_changed_ui.py

# Step 5: Compare screenshots and highlight visual differences
python compare_ui.py
```

---

## **Use Case**

This project highlights any visual UI changes, helping you catch unintended updates or layout issues early in the development lifecycle. It serves as a powerful tool for UI regression testing in CI/CD pipelines.

---

## **Future Improvements**

- Add support for headless browser mode
- Integrate diff threshold configuration
- Extend support for multiple browsers
- Export results as a test report (HTML/PDF)
- Add test suite for CI/CD integration

---

## **Author**

**Ashutosh Kumar**  
Passionate about building smart, automated solutions for real-world problems.

