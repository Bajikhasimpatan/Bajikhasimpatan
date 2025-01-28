pipeline{
agent any 

stages{
    stage('checkout'){

        steps{
            script{

                git url: 'https://github.com/Bajikhasimpatan/Bajikhasimpatan.git', branch: 'main'

            }
        }
    }
    stage('Build'){

        steps{
            script
            {
                sh "./khasim.sh"
            }

        }
    }
    stage('test'){

        steps{
            script
            {
                sh 'echo "this is the test stage"'
            }

        }
    }
    stage('deploy'){

            steps{
                script
                {
                    sh 'echo "this is the deploy stage"'
                }

            }

        }
    }
}



