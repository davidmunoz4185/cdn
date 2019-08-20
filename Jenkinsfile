pipeline {
  agent any
  stages {
    stage('Lint HTML.'){
      steps {
          sh 'tidy -q -e *.html'
      }
    }
    #stage('Upload to AWS.'){
    #  steps {
    #    withAWS(region:'eu-west-1',credentials:'aws-static') {
    #          s3Upload(bucket: 'dmm-p4', workingDir:'.', includePathPattern:'*.html');
    #    }
    #  }
    #}
  }
}
