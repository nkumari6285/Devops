pipeline{
    agent any 
        stages {
            stage('One') {
                steps{
                    echo "Hi"
                }
            }
            stage('Second'){
                steps{
                    input('Do you want to proceed')
                }
            }
            stage('Third') {
                when{
                    not{
                        branch "main"
                    }
                }
                steps {
                    echo "hello third "
                }
            }
            stage('Fourth') {
                parallel{
                    stage('Unit Testing')
                {
                        steps{
                             echo 'hello fourth'
                        }
                }
                    stage("integration"){
                        steps{
                            echo 'running integration'
                
                        }
                    }
                }
            }
        }
    }
    

            
            
            
            
