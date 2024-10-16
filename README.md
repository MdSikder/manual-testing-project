
# **Manual Testing Project: Registration Form Validation**  

This repository contains detailed **manual testing artifacts** for a registration form, demonstrating end-to-end functional testing, validation checks, and defect tracking. It includes well-documented **test cases**, **bug reports**, and **summary reports**, covering both positive and negative scenarios with real-world statuses like **Pass**, **Failed**, and **Warning**.

---

## **Table of Contents**  
1. [Project Overview](#project-overview)  
2. [Features Tested](#features-tested)  
3. [Folder Structure](#folder-structure)  
4. [Documentation](#documentation)  
5. [Reports](#reports)  
6. [How to Use](#how-to-use)  
7. [Contributing](#contributing)  
8. [License](#license)  

---

## **Project Overview**  
This project focuses on testing a **user registration form** with various input fields like **username, password, email, phone, and date of birth**. It ensures that all mandatory and optional fields are validated correctly and that both **functional requirements** and **UI/UX guidelines** are met. Additionally, it tracks **defects** identified during the test execution to ensure high-quality standards.

---

## **Features Tested**  
- Username length validation (5-15 characters)  
- Password rules (special characters, uppercase letters, minimum length)  
- Email and phone number format validation  
- Date of Birth (DOB) validation (no future dates)  
- Gender and country selection  
- Terms and conditions checkbox enforcement  
- XSS and security testing for input fields  
- Duplicate email registration prevention  

---

## **Folder Structure**  
```
/manual-testing-project
│
├── README.md                 # Project Overview and Instructions
├── reports
│   ├── summary_report.md      # Test Execution Summary Report
│   └── test_and_defect_summary_report.png  # Graphical Summary Report
└── documentation
    ├── test_cases.md          # Comprehensive Test Cases Document
    └── bug_report.md          # Detailed Bug Reports
```

---

## **Documentation**  
- [Test Cases](./documentation/test_cases.md)  
- [Bug Report](./documentation/bug_report.md)  

---

## **Reports**  
- [Summary Report](./reports/summary_report.md)  
- [Pictorial Summary](./reports/test_and_defect_summary_report.png)  

---

## **How to Use**  
1. **Clone the Repository:**
   ```bash
   git clone https://github.com/your-username/manual-testing-registration-form.git
   cd manual-testing-registration-form
   ```
2. **Explore the Documentation:**  
   Review the [test_cases.md](./documentation/test_cases.md) and [bug_report.md](./documentation/bug_report.md) files for in-depth insights.  

3. **View Reports:**  
   Check the [summary_report.md](./reports/summary_report.md) and the **pictorial summary** for an overview of the test execution and defect status.  

---

## **Contributing**  
We welcome contributions to enhance the project. To contribute:  
1. Fork the repository.  
2. Create a new branch:  
   ```bash
   git checkout -b feature/new-feature
   ```
3. Commit your changes:  
   ```bash
   git commit -m "Add a new feature or fix"
   ```
4. Push to the branch:  
   ```bash
   git push origin feature/new-feature
   ```
5. Submit a **Pull Request** for review.  

---

## **License**  
This project is licensed under the **MIT License** – see the [LICENSE](./LICENSE) file for details.  

---