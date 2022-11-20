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
                    
                    sh 'mvn clean install'
                }
            
        }
    }
}
