pipeline{
    agent any
    enviroment{
        NEW_VERSION = '1.3.0'
        SERVER-CREDENTIALS = credentials('server-credentials')
    }
    stages {
        stage('Buiid'){
            steps {
                echo 'Prasoon is Building the application....'
                echo "building version ${NEW_VERSION}" // if you want to take this variable as string use ""
                echo 'building version ${NEW_VERSION}'   
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