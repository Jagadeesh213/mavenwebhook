//e#!groovy

node {
  stage ('Checkout') {
    checkout scm
  }

  stage('Check Env Parameters'){
    echo "Branch Name : ${env.GIT_BRANCH}"
    echo "Octo Server Address : ${env.octoServer}"
  }
  //stage('Run Cake') {
  //powershell -File build.ps1 -projectName="demo" -branchName=${env.GIT_BRANCH} -octoServer=${env.octoServer} -octoApiKey=${env.octoApiKey}
  //}
  stage('Build app') {
    steps {
    //sh 'mvn clean install package'
      }
   }
}
