pipeline {
  agent any
  stages {
    stage('log tool version') {
      parallel {
        stage('log tool version') {
          steps {
            sh '''mvn --version
git --version
java --version'''
          }
        }

        stage('pom.xml') {
          steps {
            fileExists 'pom.xml'
          }
        }

      }
    }

    stage('build with maven') {
      steps {
        sh 'mvn compile test package'
      }
    }

    stage('error') {
      steps {
        writeFile(file: 'status.txt', text: 'hey i worked')
      }
    }

  }
}