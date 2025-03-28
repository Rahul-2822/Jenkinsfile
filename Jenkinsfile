pipeline { 

    agent any 

    environment { 
        EMAIL_RECIPIENT = 'rahul15sheoran@gmail.com' 
        USER_EMAIL = 'rahul15sheoran@gmail.com' 
    } 

    stages { 

        stage('Build') { 
            steps { 
                echo 'Building the application using Maven...' 
                // Example command: mvn clean package
            } 
        } 

        stage('Unit and Integration Tests') { 
            steps { 
                echo 'Running unit and integration tests using JUnit and Selenium...' 
                // Example: mvn test
            } 
        } 

        stage('Code Analysis') { 
            steps { 
                echo 'Performing static code analysis using SonarQube...' 
                // Example: sonar-scanner
            } 
        } 

        stage('Security Scan') { 
            steps { 
                echo 'Performing security scan using OWASP ZAP...' 
                // Example: zap-cli quick-scan
            } 
        } 

        stage('Deploy to Staging') { 
            steps { 
                echo 'Deploying to staging environment on AWS EC2...' 
                // Example: scp or AWS CLI command
            } 
        } 

        stage('Integration Tests on Staging') { 
            steps { 
                echo 'Running integration tests on staging using Selenium...' 
                // Example: selenium test suite execution
            } 
        } 

        stage('Deploy to Production') { 
            steps { 
                echo 'Deploying to production on AWS EC2...' 
                // Example: scp or AWS CLI command
            } 
        } 
    } 

    post { 
        success { 
            echo 'Pipeline executed successfully!' 
        } 
        failure { 
            echo 'Pipeline failed! Check the logs for more details.' 
        } 
    } 
}
