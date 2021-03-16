pipeline {
  agent any

  stages{
    
    stage ('install dependecies'){
      steps{
        echo "star install dependencies"
        sh "npm install"
      }
    }
    stage ('test'){
        steps{
          echo "run test project"
        }
    }
    stage('Build'){
      steps{
        sh 'npm run build'
      }
    }
    stage('build docker image'){
      steps{
        script{
          app = docker.build("sendykris/myreactapp")
        }
      }
    }
  }
}