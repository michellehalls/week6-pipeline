pipeline{
    agent any
    stages{
        stage("Build"){
            steps{
                echo "Build the code using a build automation tool to compile and package the code"
                echo "A tool which can be used here is Maven"
                echo "-"
            }
        }
        stage("Unit and Integration tests"){
            steps{
                echo "Run unit and integration tests"
                echo "Test automation tools could include Ansible"
            }
            post{
                success{
                    emailext to: "michelle.halls987321@gmail.com",
                    body: "The build log is attached", 
                    subject: "Unit and integration tests successful" ,
                    attachLog: true                
                }
                failure{
                    emailext to: "michelle.halls987321@gmail.com",
                    subject: "Unit and integration tests failed",
                    body: "The build log is attached",
                    attachLog: true
                }
            }
        }
        stage("Code Analysis"){
            steps{
                echo "Integrate a code analysis tool"
                echo "SonarQube is an example of a tool which can be used on Jenkins"
            }
        }
        stage("Security Scan"){
            steps{
                echo "Perform a security scan of the code"
                echo "A tool which can perform security scans is OWASP Dependency-Check"
            }
            post{
                success{
                    emailext to: "michelle.halls987321@gmail.com",
                    subject: "Security scan successful",
                    body: "The build log is attached",
                    attachLog: true
                }
                failure{
                    emailext to: "michelle.halls987321@gmail.com",
                    subject: "Security scan failed",
                    body: "The build log is attached",
                    attachLog: true
                }
            }
        }
        stage("Deploy to Staging"){
            steps{
                echo "Deploying the application to a production server"
            }
        }
        stage("Integration tests on staging"){
            steps{
                echo "Running integration tests on the staging environment"
            }
            post{
                success{
                    emailext to: "michelle.halls987321@gmail.com",
                    subject: "Integration tests on staging successful",
                    body: "The build log is attached",
                    attachLog: true
                }
                failure{
                    emailext to: "michelle.halls987321@gmail.com",
                    subject: "Integration tests on staging",
                    body: "The build log is attached",
                    attachLog: true
                }
            }
        }
        stage("Deploy to production"){
            steps{
                echo "Deploy the application to the production environment"
            }
        }
        }
}
