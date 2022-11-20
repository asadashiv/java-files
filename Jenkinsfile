pipeline {
    agent any
    tools {
        maven MAVEN_HOME
        stages{
            stage ('clone'){
                steps {
                    echo "this is clone stage"
           
                }
            }   
                stage ('Build'){
                    steps {
                    echo "this is Build stage"
                    'mvn clean install'
                    }
                }     
        }
    }
}
