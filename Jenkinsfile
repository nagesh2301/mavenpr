@Library('shared1')_
node('built-in')
{
    stage('ContDownload_master')
    {
        shared.newGit("https://github.com/intelliqittrainings/maven.git")
    }
    
     stage('ContBuild_mast')
    {
        shared.newMaven()
    }
    
}
