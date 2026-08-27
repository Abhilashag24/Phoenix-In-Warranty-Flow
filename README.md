# Postman API Automation Integration using GitHub Actions #

This repository is a demonstration for POC for integrating postman tests with GitHub Actions. The tests are written in Postman and they are executed on VM with the help of newman and newman-reporter-htmlextra.
GitHub Actions will trigger project execution on every PUSH to the main branch. You can also execute project manually using workflow-dispatch. The Project runs on the scheduled time with the help of cron jobs.

The HTML report is archived and kept in the artifacts section for the team to download it. Along with that they can view reports directly from the GitHub page: https://abhilashag24.github.io/Phoenix-In-Warranty-Flow/
The latest report is mailed to the team members using Gmail SMTP.

## About Me ##

Hi I am Abhilasha Gadgil. I’m a Senior SDET/Test Manager specializing in building scalable automation frameworks and leading high‑performance engineering teams. My work focuses on Java, Selenium, Playwright, and Chrome DevTools Protocol, with a strong emphasis on CI/CD, reliability, and future‑proof architecture. I enjoy solving complex problems, mentoring engineers, and creating systems that make testing effortless and efficient.
You can connect me over (https://www.linkedin.com/in/abhilashagadgil/)


## Testing Coverage ##

1. Happy flow Testing
2. Negative Testing and Edge Case Testing
3. Token Testing
4. Data Driven Testing using CSV
5. Schema Validation
6. Secret management with GitHub Secrets

## Tech Stack ##
1. Postman
2. Node.js V24
3. Newman
4. Newman-Reporter-Htmlextra
5. GitHub Actions
6. Gmail SMTP
7. GitHub Pages
8. CSV for data driven testing
9. AWS EC2 instance for self-hosted GitHub Runner

## GitHub Pages ##

You can directly view the latest test reports of the Postman Test at the GitHub page link: https://abhilashag24.github.io/Phoenix-In-Warranty-Flow/


   ## HTML report ##

The report will be created in Newman folder
![Postman Report](https://abhilashag24.github.io/Phoenix-In-Warranty-Flow/)

## Project Structure ##

```
Phoenix InWarrenty flow
├─ InWarrenty-flow collection QA.postman_collection.json   # Collection File
├─ QA.postman_environment.json          # Environment File
└─ testdata.csv   # TestData File

```

## How to run the Project ##

You can run the project on your local system for that:
1. Clone the project on local system: https://github.com/Abhilashag24/Phoenix-In-Warranty-Flow.git
2. Install Node.js and npm from https://nodejs.org/en/download
3. Install Newman using: ``` npm install -g newman ```
4. Install Newman-Reporter-htmlExtra using: ``` npm install -g newman-reporter-htmlextra ```
5. Run the Newman command:
    ```
               newman run 'InWarrenty-flow collection QA.postman_collection.json' \
              -e 'QA.postman_environment.json' \
              -d 'testdata.csv' \
              -r cli,htmlextra \
              --reporter-htmlextra-export ./newman/index.html
     ```

