pipeline {
    agent any

    stages {
        stage('Git Verification') {
            steps {
                git credentialsId: 'f9045a0b-afe4-4d37-9daf-0a5939a35d63', url: 'https://github.com/safaa-09/Triang07.git'
            }
        }
        
        stage('Build'){
            steps{
             // Run Maven on a Unix agent.
              bat "mvn clean compile"
                     echo " Build Stage"
                // To run Maven on a Windows agent, use
                // bat "mvn -Dmaven.test.failure.ignore=true clean package"
        }
    
    }
        }
        
        post{
always{
echo " ceci sera toujours exécuté"
}
            
failure{
    echo " ceci sera exécuté si le build échoue"
}
        }
}
