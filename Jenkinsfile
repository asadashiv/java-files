pipeline {
    agent {label 'java7'}
    
        stages {
            stage ('clone'){
                step {
                    echo "this is clone stage"
                }
            }
            stage ('Build'){
                tools {
                maven MAVEN_HOME
                step {
                    
                    echo "this is Build stage"
                    sh 'mvn clean install'
                }
            }
        }
    }
}
