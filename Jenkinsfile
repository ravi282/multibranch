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
        sh label: '', script: 'scp /var/lib/jenkins/workspace/multibranch_loan/webapp/target/webapp.war ubuntu@172.31.44.150:/var/lib/tomcat7/webapps/qaenv.war'
    }
    
    
    
    
}
