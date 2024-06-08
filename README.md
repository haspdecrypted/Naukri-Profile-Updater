# Naukri-Profile-Updater

### Overview
This Python script automates the process of logging into Naukri, navigating to the user's profile, and updating it. It uses Selenium, a popular web automation tool, to interact with the Naukri website.

### Requirements
- Python 3.x
- Selenium library (`pip install selenium`)
- Chrome WebDriver (download from [here](https://sites.google.com/a/chromium.org/chromedriver/))

### Setup
1. Install Python 3.x if not already installed.
2. Install the Selenium library by running `pip install selenium`.
3. Download the Chrome WebDriver compatible with your Chrome browser version and operating system.
4. Update the `chrome_driver_path` variable in the script with the path to the downloaded Chrome WebDriver.

### Usage
1. Run the script using Python: `python naukri_profile_updater.py`.
2. The script will open the Naukri website, log in with the provided credentials, navigate to the user's profile, and click the edit button to make changes.
3. Edit the script to provide your Naukri login credentials:
    ```python
    # Enter your Naukri login credentials here
    email_field.send_keys("your_email@example.com")
    password_field.send_keys("your_password")
    ```

### Notes
- Make sure to update the `email_field.send_keys()` and `password_field.send_keys()` lines with your actual Naukri login credentials.
- The script uses XPath to locate elements on the webpage. Make sure the XPath expressions are still valid if the structure of the Naukri website changes.
- This script is intended for educational purposes and should be used responsibly.

### Disclaimer
This script interacts with websites programmatically and may violate the terms of service of the websites being accessed. Use it at your own risk and responsibility.
