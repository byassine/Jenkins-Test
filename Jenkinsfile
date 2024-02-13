node {
    stage('Clone Repo') {
      git 'https://github.com/byassine/Jenkins-Test.git'
    }    
    stage('Deploy app on K8s') {

          sh 'kubectl apply -f $JENKINS_HOME/workspace/test/deploy.yaml'
    }
}
