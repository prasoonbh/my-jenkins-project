pipeline{
    agent any
    enviroment{
        NEW_VERSION = '1.3.0'
        SERVER-CREDENTIALS=credentials('server-credentials')
    }
    stages {
        stage('Buiid'){
            steps {
                echo 'Prasoon is Building the application....'
                withCredentials ([
                        usernamePassword(credentials: 'server-credentials', usernameVariable: USER, passwordVariable: PASSWORD)

                ])  {
                        sh "some script ${USER} ${PASSWORD}"
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
                echo "deploying with ${SERVER-CREDENTIALS}"
            }
        }
        
    }
}