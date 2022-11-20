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
                    cd /home/java/java-workspace/workspace/java_deploy
                    
                    mvn clean install
                    '''
                }
            
        }
            stage ('Deploy'){
               
                steps {
                    
                    echo "this is Deploy stagse"
                    sh '''
                    scp /home/java/java-workspace/workspace/java_deploy ubuntu@172.31.36.186:/opt/tomcat/webapps/java_deploy_hello_world_war
                    
                    '''
                }
            
        }
    }
}
