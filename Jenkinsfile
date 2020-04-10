pipeline {
    agent {
        label 'Generic'
    } //agent
    stages {
        stage("Setup scripts"){
            steps{
                sh """
                    yum install pytest
                """    
            } // steps
        } // stage
        stage("Run unit tests"){
            steps {
                sh """
                   python -m pytest
                """
            }//steps
        }//stage
    } // stages
    post {
        always {
           sh """
              yum uninstall pytest -y
            """            
        }//always
    }//post
} //pipeline