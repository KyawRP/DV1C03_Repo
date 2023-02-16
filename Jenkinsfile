

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
                              if Proceed {
                                    sh"""
                                    echo “Work Released - 22050023”
                                    """
                                         } 
		                       else {
                                      sh""
                                      Abort
                                      ""
                                    }
                            }/*script*/
                        } /*steps*/
                   }/*stage1*/
             }/*stages*/
}/*pipeline*/
  
  
