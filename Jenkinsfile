pipeline {
    agent any

    stages {

        stage('Build') {
            steps {
                echo 'Stage 1: Build'
                echo 'Task: Compiling and packaging the application source code.'
                echo 'Tool: Maven – a build automation tool used to compile Java source files, resolve dependencies, and package the application into a deployable artifact (e.g., a .jar or .war file).'
            }
        }

        stage('Unit and Integration Tests') {
            steps {
                echo 'Stage 2: Unit and Integration Tests'
                echo 'Task: Running unit tests to verify individual components function correctly, and integration tests to confirm that different modules work together as expected.'
                echo 'Tools: JUnit (unit testing framework for Java), Selenium (integration/UI test automation tool).'
            }
        }

        stage('Code Analysis') {
            steps {
                echo 'Stage 3: Code Analysis'
                echo 'Task: Analysing the source code for code quality issues, code smells, duplication, and adherence to industry coding standards.'
                echo 'Tool: Checkstyle – a static code analysis tool integrated with Jenkins via the Checkstyle Plugin to enforce coding standards and flag violations.'
            }
        }

        stage('Security Scan') {
            steps {
                echo 'Stage 4: Security Scan'
                echo 'Task: Scanning the application and its dependencies for known security vulnerabilities and CVEs.'
                echo 'Tool: OWASP Dependency-Check – a software composition analysis tool that detects publicly disclosed vulnerabilities in project dependencies.'
            }
        }

        stage('Deploy to Staging') {
            steps {
                echo 'Stage 5: Deploy to Staging'
                echo 'Task: Deploying the packaged application artifact to a staging environment that mirrors the production setup.'
                echo 'Tool: AWS CLI / SSH deployment to an AWS EC2 instance configured as the staging server.'
            }
        }

        stage('Integration Tests on Staging') {
            steps {
                echo 'Stage 6: Integration Tests on Staging'
                echo 'Task: Running integration tests against the staging environment to validate that the application behaves correctly in a production-like setting.'
                echo 'Tool: Postman / Newman – used to run automated API integration test collections against the deployed staging application.'
            }
        }

        stage('Deploy to Production') {
            steps {
                echo 'Stage 7: Deploy to Production'
                echo 'Task: Deploying the verified and tested application artifact to the live production server.'
                echo 'Tool: AWS CLI / SSH deployment to an AWS EC2 instance configured as the production server.'
            }
        }

    }
}
