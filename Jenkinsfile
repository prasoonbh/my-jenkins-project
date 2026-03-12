pipeline{
    agent any
    environment {
        NEW_VERSION = '1.3.0'
        SERVER_CREDENTIALS=credentials('server-credentials')
    }
    stages {
        stage('Build'){
            steps {
                echo 'Prasoon is Building the application....'
                withCredentials ([
                        usernamePassword(
                            credentialsId: 'server-credentials', 
                            usernameVariable: 'USER', 
                            passwordVariable: 'PASSWORD'
                            )

                ])  {
                        
                } 
            }
        }
        stage ('Test') {
            steps {
                echo 'Prasoon is in testing stage'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Prasoon is in Deploymeny stage'
                echo "deploying with ${SERVER_CREDENTIALS}"
            }
        }
        
    }
}