# postman-newman-jenkins
FIS-QATests to run on postman-newsman-jenkins

1. This repository contains JSON collections for the FIS technical test.
2. Happy Path, Negative Path and Schema Validation is done in the project.
3. This repo contains Test scenario doc, Test case sheet, Jenkins execution video. 

To run the APIs in the JSON collection,
## Software requirement

1. GIT
2. POSTMAN

## Steps Used

1. Clone or download the repo
2. Import the JSON collection in postman
3. Execute the automated tests in postman 

## API test execution in Jenkins 

1. In order to run tests in jenkins, I've used newman CLI option for postman.
2. I've created a Jenkins project, have provided GITHUB repo url and credentials to access postman collection and package.json file for newman to install dependencies and recognize the test script.
3. Shell script executed 
   ```
    export PATH="/usr/local/bin/npm:/usr/local/bin/node:/usr/local/bin:$PATH"
    npm install
    npm run api-tests-production
    ```
4. When the jenkins project is built the execution results are displayed in the console log.

**NOTE:**
Since jenkins is installed in my local machine a video is attached to show the test execution.
