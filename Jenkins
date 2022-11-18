pipeline {
    agent any
    tools {
        maven '3.8.6'

    stages{
        stage ('Build'){
            steps {
            echo "this is build stage"
            sh 'mvn clean package'
            }
            post{
                success {
                    echo "Archiving the Artifacts"
                    archiveArtifacts artifacts: '**/target/*.war'
                }
            }
            
        }
        stage ('Deploy') {
            steps {
            echo "this is Deploy stage"
           deploy adapters: [tomcat9(credentialsId: 'd78895c3-6736-4e52-bba7-53f84b395258', path: '', url: 'http://43.205.115.199:8090/')], contextPath: null, war: '**/*.war'
                
            }
            
        }
            
    }
    
}
