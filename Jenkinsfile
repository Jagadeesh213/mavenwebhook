#!groovy

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
  stage ('Initialize') {
    steps {
    sh '''
        M2_HOME=/opt/maven
        M2=/opt/maven/bin
        PATH=$PATH:$HOME/bin/:$JAVA_HOME:$M2:$M2_HOME
        export PATH
        echo "PATH = ${PATH}"
        echo "M2_HOME = ${M2_HOME}"
        whoami
        '''
        }
    }
}
