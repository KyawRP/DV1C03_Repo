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
                    docker run -d -it -p 42000:8080 --name=rp_container rp_image /bin/sh
                    docker rm -f rp_container
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
        
         stage('Exit'){
            steps{
//                 input('Do you want to proceed?')   
//                 when{
//                     not{
                          echo "Work Released - 22050023"  
//                     }
//                 }
//             }
//             steps{
//                 sh(script:"""
//                      exit 1    
//                  """)
            }
            
         }
    }
}
