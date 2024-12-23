pipeline {
    agent any
    stages {
        stage('Build Application') {
            steps {
                bat 'mvn clean install'
            }
        }
        stage('Deploy Application to Mulesoft CloudHub') {
            environment {
                ANYPOINT_CREDENTIALS = credentials('anypoint-cloudhub-credentials')
            }
            steps {
                bat """
                    mvn package deploy -DmuleDeploy -Danypoint.username=Amir122321 -Danypoint.password=Amir122306
                """
            }
        }
    }
}
