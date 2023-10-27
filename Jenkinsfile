pipeline {
  agent {
    docker {
      image 'node:18.18.2-alpine3.18'
      reuseNode: true
    }
  }
  stages {
    stage('build') {
      environment {
        name = 'Minh Ha'
        cc = """${
          sh(
            returnStdout: true,
            script: 'echo "Hi Ha Thien Minh3"'
          )
        }
        """
        exit_status = """${
          sh(
            returnStatus: true,
            script: 'exit 1'
          )
        }
        """
      }
      steps {
        sh 'echo "Hello $cc"'
        sh 'node --version'
      }
    }
    stage('build-next'){
      steps {
          sh 'printenv'
      }
    }
  }
}
