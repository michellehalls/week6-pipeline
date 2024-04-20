pipeline {
    agent any
    stages {
        stage("Build") {
            steps {
                echo "Build the code using a build automation tool to compile and package the code"
                echo "A tool which can be used here is Maven"
            }
        }
        stage("Unit and Integration Tests") {
            steps {
                echo "Run unit and integration tests"
                echo "Test automation tools could include Ansible"
            }
        }
        stage("Code Analysis") {
            steps {
                echo "Integrate a code analysis tool"
                echo "SonarQube is an example of a tool which can be used on Jenkins"
            }
        }
        stage("Security Scan") {
            steps {
                echo "Perform a security scan of the code"
                echo "A tool which can perform security scans is OWASP Dependency-Check"
            }
        }
            post {
                always {
                    echo "========always - security scan========"
            }
        }
        stage("Deploy to Staging") {
            steps {
                echo "Deploy the application to a staging server"
                sleep time: 10, unit: 'SECONDS'
            }
        }
        stage("Integration Tests on Staging") {
            steps {
                echo "Run integration tests on the staging environment"
            }
        }
        stage("Deploy to Production") {
            steps {
                echo "Deploy the application to the production server"
            }
        }
    }
}
