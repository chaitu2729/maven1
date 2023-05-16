@Library('mylibrary')_
node('built-in ')
{
    stage('continuesdownload_master')
    {
        declrative.newDownload('maven1.git')
    }
    stage('continuesbuild_master')
    {
        declrative.newBuild()
    }
    stage('continuesdeployment_master')
    {
      declrative.newDeployment("chaituscripted","172.31.18.100","testapp") 
    }
    stage('continuestesting_master')
    {
    declrative.newDownload('functional-testing.git')
    declrative.runSelenium('chaituscripted')
    }
    stage('continuesdelivery_master')
    {
      declrative.newDeployment("chaituscripted","172.31.30.2","prodapp")   
    }
    
}

