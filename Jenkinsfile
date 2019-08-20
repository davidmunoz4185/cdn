pipeline {
  agent any
  stages {
    stage('Lint HTML.'){
      steps {
          sh 'tidy -q -e *.html'
      }
    }
    stage('Build Image.'){
      steps {
          sh 'docker build -t davidmunoz4185/nginx:1.0.0 .'
      }
    }
    stage('Push Image.'){
      steps {
            script {
                docker.withRegistry('https://hub.docker.com', 'docker-id') {
                    def customImage = docker.build("davidmunoz4185/nginx:1.0.0")
                    /* Push the container to the custom Registry */
                    customImage.push()
                }
            }
        }
    }
  }
}
