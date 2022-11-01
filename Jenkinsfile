@Library('shared1')_
node('built-in')
{
    stage('ContDownload_loan')
    {
        shared.newGit("https://github.com/intelliqittrainings/maven.git")
    }
    
     stage('ContBuild_loan')
    {
        shared.newMaven()
    }
    
}
