# Project Title: List Tracker

[Link to live project here --> https://app.grocerylisttracker.com/](#https://app.grocerylisttracker.com/)

## Table of Contents
- [Project Title: List Tracker](#project-title-list-tracker)
  - [Table of Contents](#table-of-contents)
  - [Overview](#overview)
  - [Methods](#methods)
  - [Tech Stack](#tech-stack)
  - [Limitations](#limitations)
  - [Upcoming Updates](#upcoming-updates)
  - [Repository Structure](#repository-structure)
  - [Revision History](#revision-history)
    - [How to Update](#how-to-update)

## Overview
The purpose of this project is get experience deploying a simple applcation across various AWS services. Baseline function takes precedence over aesthetics for the time being. The ultimate goal is to become proficient in using CloudFormation Stacks to deploy applications. 

This simple applicaiton allows a user to create lists, add items to a list, and retrieve items from a list. 


## Methods
Project is built within a CloudFormation template. CloudFormation template is checked locally using `cfn-lint` and `aws cloudformation --validate-template`. Upon push to branch, the template is then validated and deployed to my AWS account. 

<!-- ## Function Synopsis
1. API Gateway makes call to Lambda
2. Lambda returns xzy. -->

<!-- ## DynamoDB Table Structure
**Insert table structure here.  -->


## Tech Stack
Detail the technologies and libraries used in the project.

- **Platforme**: Amazon Web Services
- **Lanauges**: Python, YAML
- **Services**:
  - `APIGateway` 
  - `Lambda`
  - `DynamoDB`
  - `S3`
  - `IAM`
  - `CloudFormation`
  - `Route53`
  


<!-- ## Installation
Instructions for setting up the project on a local machine.

1. **Clone the repository:**
   ```bash
   git clone https://github.com/username/repo.git
   cd repo

2. **Create and active a virtual environment:**
   ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows use `venv\Scripts\activate`

3. **Install dependenceies:**
    ```bash
    pip install -r requirements.txt

4. **Set up environment variables:**
    ```bash
    API_KEY=your_api_key_here
    SECRET_KEY=your_secret_key_here -->


<!-- ## Usage
Instructions for how to use the project.

1. **Step 1:**
   - details on step 1
    ```bash -->


## Limitations
- **Private Lists**: A login function has not been enabled, thus lists are not private and all lists are publicly available should a user have the ID. 

## Upcoming Updates
- **SQS**: Implement image uploading to S3 bucket where a reference to the image's location is placed in the DynamoDB table. SQS queue is placed in between the upload invocation and when a lambda function will invoke a put operation on the DDB table. 
-  




## Repository Structure

```bash
project-root/
│ 
├── api/
│   ├── templates/
│   │   ├── 404.html
│   │   ├── add-item.html
│   │   ├── add-list.html
│   │   ├── error.html
│   │   ├── get-lists.html
│   │   ├── home.html
│   │   └── success.html
│   ├── index.py
│   └── requirements.txt
├── cloudformations/
│   ├── 00_foundation.yaml
│   ├── 01_api.yaml
│   └── 01_api_generated.yaml
├── .github/workflows/
│   ├── main.yml
├── README.md
├── deployment.sh
└── .gitignore
```

## Revision History

This section documents the history of changes made to the README.

| Date       | Version | Author       | Description                                           |
|------------|---------|--------------|-------------------------------------------------------|
| 2024-08-28 | 1.0.0   | B. Fischer   | Initial creation of the repository and documentation. |
| YYYY-MM-DD | X.X.X   | Your Name    | Description of the changes made.                      |
| YYYY-MM-DD | X.X.X   | Your Name    | Description of the changes made.                      |


### How to Update

1. Add a new row to the table above for each update.
2. Increment the version number following semantic versioning (e.g., 1.0.1 for a small change, 1.1.0 for a new feature, 2.0.0 for a major update).
3. Include the date of the update, the author who made the change, and a brief description of what was updated.