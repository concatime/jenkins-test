def getDiskPoolId = { 'diskpool1' }
pipeline {
  agent none
  stages {
    stage('do') {
      agent { dockerfile { label "os:linux && ews:${getDiskPoolId()} && docker" } }
      steps {
        sh 'env | sort'
      }
    }
  }
}
