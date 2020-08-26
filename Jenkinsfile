pipeline {
  agent any
  stages{
    stage('Build') {
      steps {
        echo 'Running Build Automation'
        sh './gradlew build --no-daemon'
        archiveArtifacts artifacts: 'dist/trainSchedule.zip'
        //
      }
    }
    stage('Test') {
      steps {
        input 'Are you ok to receive the hello world message?'
        sh 'echo Hello World!'
      }
    }
  }
}
