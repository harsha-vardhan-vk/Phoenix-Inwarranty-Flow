# Postman API Automation Integration with GitHub Actions #

This repository is a demonstration for POC for Inetgrationg postman tests with github actions. The Tests are written in Postman and they are executed on the virtual machine with the help of newman and newmn-reporter-htmlextra.
GitHub Actions will trigger thew project execution on every push to the new branch. You can also execute project manually using workflow_disptch. The Project runs on a scheduled time with the help of cron job.

The HTML report is archived and kept in the artifact section for the team to download it. Along with that they can view the report directly from the github page : https://harsha-vardhan-vk.github.io/Phoenix-Inwarranty-Flow/
The latest report is mailed to the team members using GMAIL SMTP

## About Me ## 
Hi, My name is Harsha vardhan. I have 4.7 years of experience in Manual testing, currently transition towards SDET, you can connect with me in LinkedIn: https://www.linkedin.com/in/harsha-vardhana-v-k-bb662b1b7/?skipRedirect=true 

## Testing Coverage ## 
1. Happy Flow Testing
2. Negative Testing and Edge Case testing
3. Token Testing
4. Data Driven Testing with CSV
5. Schema Validation
6. Secrets management with Github Secrets

## Tech Stack ##
1. Postman
2. Nodejs 22v
3. Neman
4. Neman-Reporter-htmlextra
5. Github Actions
6. Gmail SMTP
7. Github Pages
8. CSV for Data Driven testing
9. AWS-EC2 instance foe Self hosted github runner.

## Github Pages ##
You can directly view the lates test report of the Postman Test at the Github Page link: https://harsha-vardhan-vk.github.io/Phoenix-Inwarranty-Flow/


## HTML Report ##
The Report will be created in the newman folder 
![Postman report](https://github.com/harsha-vardhan-vk/Phoenix-Inwarranty-Flow/blob/static-content/Static%20html%20extra%20image%20.png)


This can be done another way using 'GitHub raw content' like below 
![Postman report](https://raw.githubusercontent.com/harsha-vardhan-vk/Phoenix-Inwarranty-Flow/static-content/Static%20html%20extra%20image%20.png)

## Project Structure ##
```
Pheonix InWarranty flow
├─ InWarrantyFlowCollection Copy.postman_collection.json # Collection File
├─ InWarrantyFlowCollection.postman_collection.json # Collection File
├─ package-lock.json
├─ package.json
├─ QA.postman_environment.json
├─ README.md
└─ testdata.csv # TestData File

```

## How to run the project ##
You can run the project on your local system for that:
1. Clone the Project on the Local System: https://github.com/harsha-vardhan-vk/Phoenix-Inwarranty-Flow.git
2. Install NodeJs and NPM from: https://nodejs.org/en
3. Install Newman using ```  npm install -g newman ```
4. Install Newman-reporter-htmlextra ``` npm install -g newman-reporter-htmlextra ```
5. Run the Newman Command:

```
 newman run 'InWarrantyFlowCollection.postman_collection.json' \
            -e QA.postman_environment.json \
            -d testdata.csv \
            -r cli,htmlextra \
            --reporter-htmlextra-export ./newman/index.html 
```
