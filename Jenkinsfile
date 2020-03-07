node('master') 
{
    stage('ContinuousDownload_master')
    {
       git 'https://github.com/ravi282/multibranch.git'
    } 
    stage('ContinuousBuild_master')
    {
        sh label: '', script: 'mvn package'
    }
    stage('ContinuousDeployment_master')
    {
        sh label: '', script: 'scp /var/lib/jenkins/workspace/multibranch/webapp/target/webapp.war ubuntu@172.31.44.150:/var/lib/tomcat7/webapps/qaenv.war'
    }
    
    
    
    
}
