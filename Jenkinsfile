node('master') 
{
    stage('ContinuousDownload_master')
    {
       git 'https://github.com/selenium-saikrishna/maven.git'
    } 
    stage('ContinuousBuild_master')
    {
        sh label: '', script: 'mvn package'
    }
    stage('ContinuousDeployment_master')
    {
        sh label: '', script: 'scp /home/ubuntu/.jenkins/workspace/multibranch/webapp/target/webapp.war ubuntu@172.31.34.169:/var/lib/tomcat7/webapps/qaenv.war'
    }
    
    
    
    
}
