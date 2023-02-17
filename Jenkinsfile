pipeline {
    agent any

    stages {
        /*
        stage('Verify Branch') {
            
            steps {
                echo "$main"
            } 
            echo "Verify Branch:)"
        }
        */
        stage('Start build & test app') {
            steps {
                sh(script:"""
                    sudo chmod 777 /var/run/docker.sock
                    sudo chown ${USER}:docker /var/run/docker.sock
                    docker ps -a
                """)
            }
            post {
                success {
                    echo "App Started successfully :)"
                }
                failure {
                    echo "App failed to start :("
                }
            }
            
        }
        
        // stage('Run trivy') {
        //     steps {
        //        sh(script:"""
        //             trivy prasadzende/sample_repo:credit_cls     
        //        """)
        //     }            
        // }
        
    }
}
