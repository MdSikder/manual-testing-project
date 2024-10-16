# Test Case Document

Here's a detailed set of **20 test cases** for a **Registration Page**, covering both **positive and negative scenarios**. These test cases assume the registration page contains the following fields:

- **Username** (min 5, max 15 characters)
- **Password** (min 8 characters, must contain 1 uppercase, 1 number)
- **Email** (valid email format)
- **Phone Number** (10-15 digits)
- **Date of Birth**
- **Gender** (Male, Female, Other - radio button)
- **Country** (Dropdown)
- **Accept Terms and Conditions** (Checkbox)
---

| **Test Case ID** | **Test Description** | **Preconditions** | **Test Data** | **Test Steps** | **Expected Result** | **Actual Result** | **Status** | **Comments/Notes/Remarks** |
|------------------|----------------------|-------------------|---------------|----------------|---------------------|-------------------|------------|----------------------------|
| TC_01 | Verify all fields accept valid data | NA | Username: `user123`<br>Password: `Test@1234`<br>Email: `test@example.com`<br>Phone: `1234567890`<br>DOB: `1990-10-10`<br>Gender: Male<br>Country: USA | 1. Open registration page<br>2. Fill all fields<br>3. Submit | Registration successful | As expected | Pass | All fields handled valid data correctly |
| TC_02 | Verify username less than 5 characters | NA | Username: `usr`<br>Password: `Test@1234` | Enter username and submit | Error: "Username must be at least 5 characters" | Error message not displayed | Failed | Error handling issue |
| TC_03 | Verify username exceeding 15 characters | NA | Username: `verylongusername12345`<br>Password: `Test@1234` | Enter username and submit | Error: "Username must not exceed 15 characters" | Error message displayed but field accepted input | Warning | Validation partially failed |
| TC_04 | Verify password without special characters | NA | Password: `Test1234` | Enter password and submit | Error: "Password must contain at least 1 special character" | As expected | Pass | Password validation correct |
| TC_05 | Verify invalid email format | NA | Email: `invalid-email` | Enter email and submit | Error: "Invalid email format" | As expected | Pass | Validated email format |
| TC_06 | Verify phone number with less than 10 digits | NA | Phone: `12345` | Enter phone and submit | Error: "Phone number must be 10-15 digits" | Error message not aligned correctly | Warning | UI alignment issue |
| TC_07 | Verify future date as Date of Birth | NA | DOB: `2030-01-01` | Enter date of birth and submit | Error: "Invalid Date of Birth" | As expected | Pass | Validated DOB range |
| TC_08 | Verify registration without selecting gender | NA | Gender: Not selected | Skip gender selection | Error: "Please select a gender" | As expected | Pass | Gender selection validated |
| TC_09 | Verify terms and conditions checkbox not checked | NA | Terms: Not checked | Submit without accepting terms | Error: "You must accept terms" | Checkbox disabled after submission | Warning | Usability issue detected |
| TC_10 | Verify valid registration with different genders | NA | Gender: Other | Fill all fields and select 'Other' | Registration successful | As expected | Pass | Gender options work |
| TC_11 | Verify duplicate email registration | An account already exists with the same email | Email: `test@example.com` | Enter duplicate email and submit | Error: "Email already exists" | As expected | Pass | Email uniqueness validated |
| TC_12 | Verify special characters in username | NA | Username: `user@name` | Enter username and submit | Error: "Username cannot contain special characters" | Error displayed but form not blocked | Warning | Needs stricter validation |
| TC_13 | Verify registration without password | NA | Password: Empty | Leave password field empty and submit | Error: "Password is required" | As expected | Pass | Password field validation works |
| TC_14 | Verify phone number with non-numeric input | NA | Phone: `abcd1234` | Enter phone and submit | Error: "Phone number must be numeric" | As expected | Pass | Numeric validation working |
| TC_15 | Verify password without uppercase letters | NA | Password: `test@123` | Enter password and submit | Error: "Password must contain at least one uppercase letter" | As expected | Pass | Password rule enforcement works |
| TC_16 | Verify minimum password length | NA | Password: `Te@12` | Enter password and submit | Error: "Password must be at least 8 characters" | No error displayed | Failed | Length validation broken |
| TC_17 | Verify valid registration for a non-US country | NA | Country: India | Select India from the dropdown and submit | Registration successful | Dropdown was pre-selected to default country | Warning | Country dropdown UX issue |
| TC_18 | Verify form submission with empty fields | NA | All fields: Empty | Leave all fields blank and submit | Error: "All fields are required" | As expected | Pass | Mandatory field check works |
| TC_19 | Verify cross-site scripting (XSS) attempt in username | NA | Username: `<script>alert(1)</script>` | Enter XSS payload and submit | Error: "Invalid input" | As expected | Pass | XSS attack blocked |
| TC_20 | Verify password without digits | NA | Password: `Test@pass` | Enter password and submit | Error: "Password must contain at least one digit" | Error displayed but still allowed registration | Failed | Critical validation issue |

---

### **Explanation of Status Updates**

1. **Pass**: Functionality works as expected.
2. **Failed**: Functionality didn't work as expected; a major issue needs fixing.
3. **Warning**: Partially working, but there are minor issues or inconsistencies (e.g., UI issues, usability concerns).

---

### **Explanation of Columns**

- **Test Case ID**: Unique identifier for each test case.
- **Test Description**: Brief description of what the test case verifies.
- **Preconditions**: Conditions that need to be met before executing the test.
- **Test Data**: Data inputs required for executing the test.
- **Test Steps**: Sequential steps to be followed to perform the test.
- **Expected Result**: The correct system behavior as per requirements.
- **Actual Result**: What actually happened after performing the test (filled after execution).
- **Status**: Indicates whether the test case passed, failed, or has warnings.
- **Comments/Notes/Remarks**: Additional observations or remarks about the test case.