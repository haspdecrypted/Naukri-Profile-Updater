from selenium import webdriver
from selenium.webdriver.common.by import By
from selenium.webdriver.chrome.service import Service
from selenium.webdriver.support.ui import WebDriverWait
from selenium.webdriver.support import expected_conditions as EC
import time

# Update this path to the location of your chromedriver
chrome_driver_path = “path/to/chromedriver"

# Set up the Chrome WebDriver
service = Service(chrome_driver_path)
driver = webdriver.Chrome(service=service)

try:
    # Open Naukri website
    driver.get('https://www.naukri.com/')
    print("Naukri website opened.")

    # Wait for the login button to be clickable and click it
    login_button = WebDriverWait(driver, 10).until(
        EC.element_to_be_clickable((By.XPATH, "//a[contains(text(), 'Login')]"))
    )
    login_button.click()
    print("Login button clicked.")

    time.sleep(2)

    # Wait for the login fields to be present
    email_field = WebDriverWait(driver, 10).until(
        EC.presence_of_element_located((By.XPATH, "/html/body/div[1]/div[4]/div[2]/div/div/div[2]/div/form/div[2]/input"))
    )
    password_field = WebDriverWait(driver, 10).until(
        EC.presence_of_element_located((By.XPATH, "/html/body/div[1]/div[4]/div[2]/div/div/div[2]/div/form/div[3]/input"))
    )
    print("Login fields found.")

    # Enter credentials
    email_field.send_keys("user”_key)
    password_field.send_keys(“password_key”)
    print("Credentials entered.")

    # Find and click the submit button
    submit_button = WebDriverWait(driver, 10).until(
        EC.element_to_be_clickable((By.XPATH, "//button[@type='submit']"))
    )
    submit_button.click()
    print("Submit button clicked.")

    time.sleep(2)

    # Wait for the profile button to be present and click it
    profile_button = WebDriverWait(driver, 20).until(
        EC.element_to_be_clickable((By.XPATH, "/html/body/main/div/div/div[3]/div/div[3]/div[2]/a"))
    )
    profile_button.click()
    print("Profile button clicked.")

    time.sleep(2)

    # Wait for the edit button (pen icon) to be present and click it
    edit_button = WebDriverWait(driver, 20).until(
        EC.element_to_be_clickable((By.XPATH, "/html/body/div[3]/div/div/span/div/div/div/div/div/div[1]/div[1]/div/div/div/div[2]/div[1]/div/div[1]/em"))
    )
    edit_button.click()
    print("Edit button clicked.")

    time.sleep(2)

    # Wait for the save button to be present and click it
    save_button = WebDriverWait(driver, 10).until(
        EC.element_to_be_clickable((By.XPATH, "/html/body/div[6]/div[10]/div[2]/div/form/div[8]/div/button"))
    )
    save_button.click()
    print("Save button clicked.")

    # Wait to ensure save action is completed
    time.sleep(2)

finally:
    # Close the browser
    driver.quit()
    print("Browser closed.")
