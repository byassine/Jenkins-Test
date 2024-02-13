node {
    stage('Clone Repo') {
      git 'https://github.com/byassine/Jenkins-Test.git'
    }    
    stage('Deploy to Cluster') {
        steps {
          sh 'envsubst < deploy.yaml | kubectl apply -f -'
        }
    }
}
