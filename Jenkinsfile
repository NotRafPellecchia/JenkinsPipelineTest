pipeline{
    agent any
    environment{
        MYNAME = "Raff"
    }
    parameters{
        string(name: 'Password', defaultValue: '', description: 'Value of password')
        choice(name: 'Gender', choices:['Male', 'Female'], description: 'Gender: ')
    }

    stages{
        stage("Build"){
            steps{
                echo "========executing A========"
                echo "Building from: ${MYNAME}"
            }
            post{
                always{
                    echo "========always========"
                }
                success{
                    echo "========A executed successfully========"
                }
                failure{
                    echo "========A execution failed========"
                }
            }
        }
        stage("Test"){

            when{
                expression{
                    MYNAME == "Raff"
                }
            }
            steps{
                echo "Testing App"
            }
        }

        stage("Deploy"){

            when{
                expression{
                    params.Password == "Admin"
                }
            }

            steps{
                echo "Deploying app"
            }

        }
    }
    post{
        always{
            echo "========always========"
        }
        success{
            echo "========pipeline executed successfully ========"
        }
        failure{
            echo "========pipeline execution failed========"
        }
    }
}
