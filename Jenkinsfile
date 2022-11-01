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
        shared.newDeploy("${env.WORKSPACE}","172.31.21.218","testapp1")
    }
    
         stage('ContTest_master')
    {
        shared.newGit("https://github.com/intelliqittrainings/FunctionalTesting.git")
        shared.newSelenium("${env.WORKSPACE}")
                    
    }
    
     stage('ContDeploy_mast')
    {
        shared.newDeploy("${env.WORKSPACE}","172.31.16.13","prodapp1")
    }
}

