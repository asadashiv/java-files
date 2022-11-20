pipeline {
    agent {label 'java7'}
    tools {
        maven /usr/share/maven
        stages {
            stage ('clone'){
                step {
                    echo "this is clone stage"
                }
            }
            stage ('Build'){
                step {
                    echo "this is Build stage"
                    mvn clean install
                }
            }
        }
    }
}
