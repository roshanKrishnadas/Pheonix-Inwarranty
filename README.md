# Postman API Automation Integration with Github Action #


This repository is demonstration for POC for integrerating postman tests with github actions.The test are written to Postman and they are executed on VM with the help of newman and newman-reporter-htmlextra.
Github Actions will trigger the project execution on every push to the main branch.You can also execute the project manually using workflow_dispatch.The project runs on a scheduled time with the help of cron job.

The HTML report is archive and kept in artifact section for the team to download it.Along that they can view the report directly from the github page :https://roshankrishnadas.github.io/Pheonix-Inwarranty/.
The latest report is mailed to the members using GMAIL SMTP.

## Test Coverage ##
1.Happy Flow Testing  
2.Negative Testing and Edge case Testing  
3.Token Testing   
4.Data driven Testing with csv  
5.Schema validation  
6.Secrets management with Github Secrets


## Tech Stack #
1.Postman  
2.Nodejs 22v  
3.Newman  
4.Newman-Report-Htmlextra  
5.GitHub Actions  
6.Gmail SMTP  
7.Github Pages    
8.CSV for Data Driven Testing  
9.AWS-EC2 instance for self hosted github runner.

## Github Page #
You can directly view the latest test report of the postman test at the github link : https://roshankrishnadas.github.io/Pheonix-Inwarranty/.

## HTML Report ##
The Report will be created in the newman folder
![Postman](https://github.com/roshanKrishnadas/Pheonix-Inwarranty/blob/static-branch/newman%20report.png)
<!-- ![Postman](https://raw.githubusercontent.com/roshanKrishnadas/Pheonix-Inwarranty/static-branch/newman%20report.png) -->


## Project Structure ##
```
Pheonix Inwarranty Flow
├─ Inwarranty flow CLI.postman_collection.json #colection file
├─ Inwarranty flow.postman_collection.json #collection file for data driven
├─ QA.postman_environment.json #Environment varaible
└─ TemplateD1.csv # template

```


## How to run the Project ##
You can the project on your local system for that:  
1.Clone the Project on Local System: https://github.com/roshanKrishnadas/Pheonix-Inwarranty.git  
2.Install Nodejs and NPM from https://nodejs.org/en   
3.Install Newman using ``` npm install -g newman  ```  
4.Install Newman-Reporter-htmlextra ``` npm install -g newman-reporter-htmlextra  ```  
5.Run the Newman Command: 
```
         newman run "Inwarranty flow CLI.postman_collection.json" \   
          -e "QA.postman_environment.json" \  
          -r cli,htmlextra \  
          --reporter-htmlextra-export ./newman/index.html
``` 








