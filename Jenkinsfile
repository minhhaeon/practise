pipeline {
  agent any
  stages {
    stage('build') {
      environment {
        name = 'Minh Ha'
        cc = """${
          sh(
            returnStdout: true,
            script: 'echo "Hi $name"'
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
      }
    }
    stage('build-next'){
      steps {
          sh 'printenv'
      }
    }
  }
}
