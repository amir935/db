pipeline {
    agent any
    environment {
        ANYPOINT_CREDENTIALS = credentials('anypoint-cloudhub-credentials')
    }
    stages {
        stage('Deploy CloudHub') {
            steps {
                bat """
                    mvn clean deploy -DmuleDeploy 
                """
            }
        }
    }
}
