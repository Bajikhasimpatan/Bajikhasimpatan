pipeline{
agent any 
    parameters {
  
        string(name: 'Name', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
    }
  
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
                sh """
                chmod +x khasim.sh
                ./khasim.sh ${Name}
                """
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



