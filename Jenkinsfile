pipeline {
    agent {label 'java7'}
    tools {
    maven 'maven'
    }
    
        stages {
        
             stage ('clone1'){
                  
                steps {
                    echo "this is clone stage"
                    
                }
            }
            stage ('Build'){
               
                steps {
                    
                    echo "this is Build stagse"
                    sh '''
                    cd /home/java/java-workspace/workspace/java_deploy
                    
                    mvn clean install
                    '''
                }
            
        }
            stage ('Deploy'){
               
                steps {
                    sshagent(['deploy_java']) {
                     sh "scp /home/java/java-workspace/workspace/java_deploy/dist/hello-world.war ubuntu@172.31.36.186:/opt/tomcat/webapps"
                    }
             
                    echo "this is Deploy stagse"
                
                }
            
        }
    }
}
