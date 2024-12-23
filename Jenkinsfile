pipeline {
    agent any
    environment {
        ANYPOINT_CREDENTIALS = credentials('anypoint-cloudhub-credentials')
    }
    stages {
        stage('Deploy CloudHub') {
            steps {
                bat """
                    mvn clean deploy -DmuleDeploy ^
                    -Danypoint.username=${ANYPOINT_CREDENTIALS_USR} ^
                    -Danypoint.password=${ANYPOINT_CREDENTIALS_PSW}
                """
            }
        }
    }
}
