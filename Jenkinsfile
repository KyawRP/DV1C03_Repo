

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
            steps {
                    script {
                    if (BRANCH_NAME == 'main') {
                        echo 'Hello from main branch'
                         }  
		    else {
                        sh "echo 'Hello from OK!'"
                         }
                    }/*script*/
                        } /*steps*/
                   }/*stage1*/
             }/*stages*/
}/*pipeline*/
  
  
