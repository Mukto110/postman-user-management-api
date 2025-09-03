API Testing Project with CI/CD

This is a demo API testing project built with Postman + Newman where I’ve automated multiple API workflows using both reqres.in and fakestoreapi.com.

The project covers:
* API chaining
* Authentication using tokens
* Data-driven testing
* CI/CD with GitHub Actions + Jenkins
* Automated HTML reports

🔹 What I’ve Done ->
1. User Management (reqres.in)
Full CRUD APIs
API chaining: One API’s output becomes the next API’s input
Both positive & negative test cases

2. Authentication (reqres.in)
Login & Register APIs
Token handling for secure calls

3. Data-Driven Testing (fakestoreapi.com)
Used product_data.json for multiple data sets
Perfect for testing with multiple inputs at once


📂 Project Structure
├── collections/          # Postman collections (User Mgmt, Auth, Data-Driven)
├── configs/              # Environment files for different setups
├── data_sets/            # JSON/CSV files for data-driven tests
├── reports/              # Auto-generated HTML reports
├── .github/workflows/    # GitHub Actions pipeline config
└── package.json          # Dependencies for Newman


⚡ Run Tests with Newman
Make sure you have Node.js (LTS) and Newman installed.

Here are the commands I use:

🟢 User Management Tests
<details> <summary>Click to copy command</summary>
newman run collections/01_User_Management.postman_collection.json \
  -e configs/qa_env.postman_environment.json \
  -r htmlextra \
  --reporter-htmlextra-export reports/User_Management_Test_Report.html \
  --reporter-htmlextra-browserTitle "User Management Test Report" \
  --reporter-htmlextra-title "User Management API Test Summary"
  </details>

🟢 Authentication Tests
<details> <summary>Click to copy command</summary>
newman run collections/02_Authentication.postman_collection.json \
  -e configs/qa_env.postman_environment.json \
  -r htmlextra \
  --reporter-htmlextra-export reports/Authentication_Test_Report.html \
  --reporter-htmlextra-browserTitle "Authentication Test Report" \
  --reporter-htmlextra-title "Authentication API Test Summary"
  </details>

🟢 Data-Driven Tests
<details> <summary>Click to copy command</summary>
  newman run collections/03_Data_Driven.postman_collection.json \
  -e configs/qa_env.postman_environment.json \
  -d data_sets/product_data.json \
  -r htmlextra \
  --reporter-htmlextra-export reports/Data_Driven_Test_Report.html \
  --reporter-htmlextra-browserTitle "Data Driven Test Report" \
  --reporter-htmlextra-title "Data Driven API Test Summary"
  </details>



  ⚙️ CI/CD Integration
  
GitHub Actions
Runs all tests automatically on push or pull request
Generates HTML reports as artifacts
Uses the latest Node.js LTS for reliability

Jenkins (Local)
Added for local CI/CD learning
Same tests, triggered manually


📊 Test Coverage
User Management: CRUD + chaining
Authentication: Login, Register, Token handling
Data-Driven: Multiple product data sets with fakestoreapi.com
Edge Cases: Negative and boundary testing

📜 Reports
All tests generate HTML reports
Easy to read with summary + detailed view

![GitHub Workflow Status](https://img.shields.io/github/actions/workflow/status/Mukto110/postman-user-management-api/api-tests.yml?branch=main)
![Newman Tests](https://img.shields.io/badge/Newman-Tests-blue)
![Reports](https://img.shields.io/badge/Reports-HTML-success)

🚩 Next Plans
Add API mocking for custom scenarios
Run tests in parallel for faster feedback

This project is a simple but complete demo of how to do real-world API testing with automation + CI/CD pipelines.
