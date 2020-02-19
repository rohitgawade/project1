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
    sh label: '', script: 'scp /home/ubuntu/.jenkins/workspace/multi_master/webapp/target/webapp.war  ubuntu@172.31.35.106:/var/lib/tomcat8/webapps/test.war'
    }
    stage('ContinuousTesting')
    {
        git 'https://github.com/intelliqittrainings/FunctionalTesting.git'
     
     }

}
