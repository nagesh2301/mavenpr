@Library('shared1')_
node('built-in')
{
    stage('ContDownload_mast')
    {
        shared.newGit("https://github.com/intelliqittrainings/maven.git")
    }
    
     stage('ContBuild_mast')
    {
        shared.newMaven()
    }
    
         stage('ContDeploy_master')
    {
        shared.newDeploy("${env.WORKSPACE}","172.31.11.59","testapp1")
    }
    
         stage('ContTest_master')
    {
        shared.newGit("https://github.com/intelliqittrainings/FunctionalTesting.git")
        shared.newSelenium("${env.WORKSPACE}")
                    
    }
    
     stage('ContDeploy_mast')
    {
        shared.newDeploy("${env.WORKSPACE}","172.31.1.90","prodapp1")
    }
}

