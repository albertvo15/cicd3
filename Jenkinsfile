pipeline {
    agent { docker { image 'golang' } }
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
              sh "go build -ldflags '-s' "
            }
        }
    }
}
