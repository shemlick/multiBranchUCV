pipeline {
  agent any
  stages {
    stage('for main branch') {
      when {
        branch 'main'
      }
      steps {
        echo 'main branch'
        buildName "2.0.${env.BUILD_ID}"
      }
    }
    stage('for stage branch') {
      when {
        branch 'stage'
      }
      steps {
        echo 'stage branch'
        buildName "1.9.${env.BUILD_ID}"
      }
    }
    stage('for pull request') {
      when {
        changeRequest()
      }
      steps {
        echo 'pull request'
      }
    }
  }
}
