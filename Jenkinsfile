node('master') 
{
    stage('ContinuousDownload') 
    {
       git 'https://github.com/rohitgawade/project1.git'
    }
    stage('ContinuousBuild')
    {
        sh label: '', script: 'mvn package'
    }
    stage('deploy')
    {
    sh label: '', script: 'scp /home/ubuntu/.jenkins/workspace/multi_loan/webapp/target/webapp.war  ubuntu@172.31.35.106:/var/lib/tomcat8/webapps/test1.war'
    }
    stage('testing')
    {
    git 'https://github.com/intelliqittrainings/FunctionalTesting.git'
    }

     
}
