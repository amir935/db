pipeline {
    agent any
    
    stages {
        stage('Deploy CloudHub') {
            steps {
                bat """
                   mvn clean deploy -DmuleDeploy -Danypoint.username=Amir122321 -Danypoint.password=Amir122306
                """
            }
        }
    }
}
