# API Testing Project with CI/CD

This demo project shows automated API testing for a user management system (reqres.in) using Postman and Newman with a CI/CD pipeline.

## What I've Done

### API Testing
* Implemented full CRUD operations with API chaining
* Done authentication system (login and register) with token handling
* Handled positive, negative, and edge cases for all endpoints
* Used environment and global variables for better test management

### CI/CD Implementation
* Set up GitHub Actions pipeline for automated testing
* Configured Newman to run Postman collections automatically
* Generated HTML reports for easy test result viewing
* Created Jenkins job locally for additional automation

## Project Structure

```
├── collections/          # Postman collection files
├── configs/             # Environment and global variables
├── reports/             # Generated HTML test reports
├── .github/workflows/   # CI/CD pipeline configuration
└── package.json         # Newman dependencies
```

## How It Works

1. **Push code** to GitHub
2. **Pipeline triggers** automatically
3. **Newman runs** all API tests
4. **HTML reports** generated and stored
5. **Results available** in GitHub Actions

## Technologies Used

* **Postman** - API testing and collection management
* **Newman** - Command line Postman runner
* **GitHub Actions** - CI/CD automation
* **Jenkins** - Local automation setup
* **reqres.in** - Test API endpoints

## Test Coverage

* **User Management**: Complete CRUD with API chaining
* **Authentication**: Login/register with token validation
* **Edge Cases**: Comprehensive negative and boundary testing

---

*This project demonstrates automated API testing practices with modern CI/CD workflows.*
