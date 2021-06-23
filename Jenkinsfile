pipeline{
  agent any

  stages{
    stage('Maven Build'){
      steps{
        sh "mvn clean package"
      }
    }

    stage('Docker Build Image'){
      steps{
        sh "docker build . -t Docker/2021myapp:${getLatestCommitId()}"
      }
    }
    
    stage('push to docker hub'){
      steps{
        echo"deploy to dev"
        }
    }

    stage('dev-deploy'){
      steps{
       echo"deploy to uat"
        }
       }
   }
}
