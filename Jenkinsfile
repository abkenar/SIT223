//comment 2
pipeline{
    agent any
    stages{
        stage('Build') {
            steps {
                echo 'Building the code using Maven'
            }
        }
        stage('Unit and Integration Tests') {
            steps {
                echo 'Running unit and integration tests using JUnit and Selenium'
            }
            post{
                always{
                    emailext body: 'Test Message',
                    subject: 'Test Subject',
                    to: 'amin.abken@gmail.com',
                    attachLog: true
                }
            }
        }
    }

}