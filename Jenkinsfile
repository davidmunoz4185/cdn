pipeline {
  agent any
  stages {
    stage('Lint HTML.'){
      steps {
          sh 'tidy -q -e *.html'
      }
    }
    stage('Build Docker Image.'){
      steps {
          sh 'docker build -t davidmunoz4185/nginx:1.0.0 .'
      }
    }
  }
}
