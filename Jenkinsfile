pipeline{
agent any 
    parameters {
  
        string(name: 'Name', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
        string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')

        text(name: 'BIOGRAPHY', defaultValue: '', description: 'Enter some information about the person')

        booleanParam(name: 'TOGGLE', defaultValue: true, description: 'Toggle this value')

        choice(name: 'CHOICE', choices: ['One', 'Two', 'Three'], description: 'Pick something')

        password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')
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



