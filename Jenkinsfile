pipeline {
    agent { docker { image 'golang' } }
    environment {
      registry = "albertvo/test"
      registryCredential = 'dockerhub'
      XDG_CACHE_HOME ="/tmp/.cache"
    }
    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }
        stage('Build'){
            steps {
              echo 'Building Executable'
            //Produced binary is $GOPATH/src/cmd/project/project
//            sh """cd $GOPATH/src/cmd/project/ && go build -ldflags '-s'"""
//              sh "go build -ldflags '-s' "
              sh "go build"
            }
        }
    }
}
