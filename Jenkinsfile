pipeline {
    agent any
    stages {
        stage("Clean Up") {
            steps {
                deleteDir()
            }
        }
      stage("Clone Repo") {
            steps {
                script {
                    // Use the checkout step to clone the repository
                    checkout([
                        $class: 'GitSCM',
                        branches: [[name: '*/master']],
                        userRemoteConfigs: [[url: 'https://github.com/fiza-02/jenkins-maven.git']]
                    ])
                }
            }
        }
        stage("yasmin build")
        {
            steps
            {
                echo 'Hello world'
                
                  bat "echo '%PATH%'"
                    bat ' mvn clean install'
            
                 
            }
        }
     
          
    }
    
}

