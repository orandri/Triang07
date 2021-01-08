pipeline {
    agent any

    stages {
        stage('Checking github') {
            steps {
                // Get some code from a GitHub repository
                git credentialsId: 'git_credentials', url: 'https://github.com/safaa-09/Triang07.git'

            }
        }
        
        stage('Building'){
            steps{
             // Run Maven on a Unix agent.
                echo "Je suis sur la branche Master"
                sh 'mvn compile'
            }
                // To run Maven on a Windows agent, use
                // bat "mvn -Dmaven.test.failure.ignore=true clean package"
        }
     
    }
    
    post{
        
        always{
            echo 'ce message devra toujours s\'afficher'
        }
        
        success{
            echo 'ce message s\'affichera en cas de succès'
            
        }
        
        failure{
            
            echo 'ce message s\'affichera en cas d\'échec'
        }
    }
 
}
