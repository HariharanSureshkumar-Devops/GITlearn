pipeline {
    agent any
    //ENvironment Variables BLock 
    environment {
        ENV_VAR1 = 'env var-1 value'
        ENV_VAR2 = 'env var-2 value'
        ENV_VAR3 = 'env var-3 value'
    }
    // Parameters Block 
    stages {
        stage('Build') {
            steps {
                echo 'Building the application...'
                echo  " The name of ENV_VAR1 is : ${ENV_VAR1}"
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
                echo " The name of ENV_VAR2 is : ${ENV_VAR2}"
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
                echo " The name of ENV_VAR3 is : ${ENV_VAR3}"
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
