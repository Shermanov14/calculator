pipeline {
    agent {
        label 'Generic'
    } //agent
    stages {
        stage("Setup scripts"){
            steps{
                sh """
                    sudo pip install pytest 
                """    
            } // steps
        } // stage
        stage("Run unit tests"){
            steps {
                sh """
                   sudo python -m pytest
                """
            }//steps
        }//stage
    } // stages
    post {
        always {
           sh """
              sudo pip uninstall pytest -y
            """            
        }//always
    }//post
} //pipeline
