pipeline{
    agent any
    stages{
        stage("Build"){
            steps{
                echo "========Building========"
                sh "python3 hello.py"
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
            steps{
                echo "=========testing the build=========="
            }
            post{
                always{
                    echo "=========always========="
                }
                success{
                    echo "=========Tested successfully ========="
                }
            }
        }
        stage("Deploy"){
            steps{
                echo "=========deploying the artifact============"
            }
            post{
                always{
                    echo "=========always========="
                }
                success{
                    echo "=========Tested successfully ========="
                }

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