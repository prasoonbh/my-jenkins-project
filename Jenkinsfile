CODE_CHANGES = getGitChanges()

pipeline{
    agent any

    stages {
        stage('Buiid'){
            when {
                expression{
                    BRANCH_NAME= 'dev' && CODE_CHANGES == true
                }
            }
            steps {
                echo 'Prasoon is Building the application....'

            }

        }

        stage ('Test') {
            when {
                expression {
                    BRANCH_NAME  == 'DEV' || BRANCH_NAME  == 'MASTER'
                }
            }
            steps {
                echo 'Prasoon is in testing stage'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Prasoon is in Deploymeny stage'
            }
        }
        
    }
}