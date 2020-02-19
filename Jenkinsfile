de('master') 
{
    stage('ContinuousDownload') 
    {
       git 'https://github.com/rohitgawade/project1.git'
    }
    stage('ContinuousBuild')
    {
        sh label: '', script: 'mvn package'
    }
  
}
