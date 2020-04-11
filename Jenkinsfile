pipeline {
    agent {
        label 'Generic'
    } //agent
    stages {
        stage("Setup scripts"){
            steps{
                sh """
                    sudo yum install pytest -y
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
              sudo yum uninstall pytest -y
            """            
        }//always
    }//post
} //pipeline
