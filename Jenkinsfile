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
                    docker ps -a
                    docker run -d -it -p 42000:8080 --name=s2_22050023_server 22050023_webimage /bin/sh
                    docker rm s2_22050023_server
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
