pipeline {
    agent any
    
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
