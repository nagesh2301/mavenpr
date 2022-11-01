@Library('shared1')_
node('built-in')
{
    stage('ContDownload_master')
    {
        shared.newGit("https://github.com/intelliqittrainings/maven.git")
    }
    
     stage('ContBuild_master')
    {
        shared.newMaven()
    }
    
         stage('ContDeploy_master')
    {
        shared.newDeploy("scriptedshared1","172.31.21.218","testapp1")
    }
    
         stage('ContTest_master')
    {
        shared.newGit("https://github.com/intelliqittrainings/FunctionalTesting.git")
        shared.newSelenium("sharedjob")
                    
    }
    
     stage('ContDeploy_master')
    {
        shared.newDeploy("sharedjob","172.31.16.13","prodapp1")
    }
}

