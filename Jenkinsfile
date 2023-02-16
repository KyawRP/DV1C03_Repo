

pipeline {
    agent any

    stages {

        stage('Stage_1') {
            steps {
                    /* cleanWs() */
                    sh"""
                    echo “S1_22050023 : Environment Preparation Completed”
                    """
                          } /*steps*/
                   }/*stage1*/
        
        stage('Stage_2') {
		agent {
                       docker {
                           image 'gradle:6.7-jdk11'
                    // Run the container on the node specified at the
                    // top-level of the Pipeline, in the same workspace,
                    // rather than on a new node entirely:
                          reuseNode true
                               }
                      }
                   }/*stage1*/
             }/*stages*/
}/*pipeline*/
  
  
