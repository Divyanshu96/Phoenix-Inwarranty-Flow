# Postman API Automation Integration with Github Actions #

This repository is a demonstration for POC for integrating postman tests with github actions. The Tests are written in Postman and they are executed on the VM with the help of newman and newman-reporter-htmlextra.
Github Actions will trigger the project execution on every push to the main branch. You can also execute the project manually using workflow_dispatch. The projects runs on a scheduled time with the help of a cron job.

The HTML report is archived and kept in the artifact section for the team to download it. Along with that they can view the report directly from the github page : https://divyanshu96.github.io/Phoenix-Inwarranty-Flow/
The latest report is mailed to the team member using GMAIL SMTP.

## About Me ##
Hi My name is Divyanshu Sharma. I have 4 years of experience in Automation Testing. My Skillset Includes UI Automation with Selenium WebDriver and for API Testing I use Postman.
You can connect with me over: https://www.linkedin.com/in/divyanshusharma18/

## Testing Coverage ##
1. Happy Flow Testing
2. Negative Testing and Edge Case Testing
3. Token Testing
4. Data Driven Testing with CSV
5. Schema Validation
6. Secrets Management with Github Secrets

## Tech Stack ##
1.Postman
2.Node.Js 22v
3.Newman
4.Newman-Reported-HtmlExtra
5.Github Actions
6.Gmail SMTP
7.Github Pages
8. CSV for Data Driven Testing
9. AWS Instance for Self Hosted github runner.

## Github Pages ##
You can directly view the latest test report of the Postman Test at the Github Page Link : https://divyanshu96.github.io/Phoenix-Inwarranty-Flow/

## HTML Report ##
The Report will be created in the newman folder
![Postman Report](https://github.com/Divyanshu96/Phoenix-Inwarranty-Flow/blob/Static-Content/Newman_Report.png)

## Project Structure ##

```
Phoenix in warranty flow
├─ InWarrantyFlowCollection.postman_collection.json #CollectionFile
├─ QA.postman_environment.json #EnvironmentFile
└─ testdata.csv #TestDataFile

```

## How to run the Project? ##
You can run the project on your local system for that:
1. Clone the Project on Local System : https://github.com/Divyanshu96/Phoenix-Inwarranty-Flow.git
2. Install NodeJs and NPM from https://nodejs.org/en/download
3. Install Newman using ```npm install -g newman```
4. Install Newman-reporter-htmlextra ```npm install -g newman-reporter-htmlextra```
5. Run the newman command :
   
             newman run 'InWarrantyFlowCollection.postman_collection.json' \
            -e QA.postman_environment.json \
            -d testdata.csv \
            -r cli,htmlextra \
            --reporter-htmlextra-export ./newman/index.html


