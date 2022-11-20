pipeline {
    agent {label 'java7'}
    tools {
    maven 'maven'
    }
    
        stages {
           
            stage ('clone'){
                parallel {
                    stage ('clone1'){
                        steps {
                        sh " this is parallel"
                        }
                    }
                    stage ('clone2'){
                        steps {
                            sh ''' 
                            ls-lrt>clone2>temp
                            cat temp
                        }
                    }
                        
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
                      
                    sh ''' 
                    scp  /home/java/java-workspace/workspace/java_deploy/dist hello-world.war ubuntu@172.31.36.186:/opt/tomcat/webapps 
                    echo "this is Deploy stagse"
                    
                    '''
                }
            
        }
    }
}
