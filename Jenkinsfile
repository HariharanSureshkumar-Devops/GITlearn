pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo 'Building the application...'
            }
            post {
                success{
                    echo "Build Successful"
                }
                failure{
                    echo "Build Failed"
                }
            }
        }
        stage('Test') {
            steps {
                echo 'Running tests...'
            }
            post{
                success{
                    echo "Tests Passed"
                }
                failure{
                    echo "Tests Failed"
                }
            }
        } // EOD 
        stage('Deploy') {
            steps {
                echo 'Deploying application...'
            } // EDO Steps
            post{
                success{
                    echo "Deployed Successfully"
                }
                failure{
                    echo "Deployment Failed"
                }
            }
        } //EOD Stage Deploy
    } //EOD Stages 
// POST BLOCK 
    post {
        always{
            echo "This will run always"
        }
        success{
            echo "This is Success "
        }
        failure {
            echo "This is Failure"

        }
    }

    } // EOD pipeline
