

pipeline {
    agent any

    stages {

        stage('Cleanup Workspace') {
            steps {
                    cleanWs()
                    sh"""
                    echo "Cleaned Up Workspace for ${APP_NAME}"
                    """
            }
        }
}
  
  
