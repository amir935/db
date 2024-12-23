pipeline {  
    agent any 
    environment {
        ANYPOINT_CREDENTIALS = credentials('anypoint-cloudhub-credentials')
    }
    stages { 
        stage('Build Application') { 
            steps { 
                bat 'mvn clean' 
            } 
        } 
        stage('Deploy CloudHub') { 
            steps { 
                echo 'Deploying Mule project due to the latest code commit...' 
                echo 'Deploying to the configured environment...' 
                bat """
                    mvn clean deploy -DmuleDeploy ^
                    -Dusername=${ANYPOINT_CREDENTIALS_USR} ^
                    -Dpassword=${ANYPOINT_CREDENTIALS_PSW} ^
                    -Dmule.http.socketTimeout=600000
                """
            }  
        } 
    } 
}
