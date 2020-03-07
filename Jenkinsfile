node('loan') 
{
    stage('ContinuousDownload_loan')
    {
       git 'https://github.com/ravi282/multibranch.git'
    } 
    stage('ContinuousBuild_loan')
    {
        sh label: '', script: 'mvn package'
    }
    stage('ContinuousDeployment_loan')
    {
        sh 'scp /var/lib/jenkins/workspace/multibranch_loan/webapp/target/webapp.war ubuntu@172.31.36.204:/home/ubuntu/var/lib/tomcat7/webapps/qaenv.war'
    }
    
    
    
    
}
