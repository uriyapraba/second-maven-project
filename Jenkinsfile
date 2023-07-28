pipeline
{
    agent
    {
        label 'slave2'
    }
    tools
    {
        maven 'maven_3.6.3'
    }
    stages
    {
        stage('GIT_CHECKOUT')
        {
            steps
            {
                checkout scmGit(branches: [[name: 'origin/master']],
                userRemoteConfigs: [
                    [ url: 'https://github.com/uriyapraba/second-maven-project.git' ]
                ])
            }
        }
        stage('Maven_Build')
        {
            steps
            {
                sh 'mvn clean install'
            }
        }
    }
}