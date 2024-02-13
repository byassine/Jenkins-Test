node {
    stage('Clone Repo') {
      git 'https://github.com/byassine/Jenkins-Test.git'
    }    
    stage('Deploy app on K8s') {
      steps{
        withKubeConfig([credentialsId: 'my-AKS-cred']) {
          sh 'kubectl apply -f $JENKINS_HOME/workspace/test/deploy.yaml'
        }
      }
    }
}
