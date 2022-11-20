pipeline {
    agent {label 'java7'}
    tools {
    maven 'maven'
    }
    
        stages {
            stage ('clone'){
                steps {
                    echo "this is clone stage"
                    
                }
            }
            stage ('Build'){
               
                steps {
                    
                    echo "this is Build stagse"
                    sh '''
                    cd /home/java/java-workspace/workspace/java deploy
                    
                    mvn clean install
                    '''
                }
            
        }
    }
}
