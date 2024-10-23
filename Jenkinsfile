pipeline {
    agent any

    tools {
        maven 'Maven'    
    }
    
    stages {
        stage("build front") {
            steps {
              echo 'building the app with yarn'
              nodejs('Node-23.0.0') {
                  sh 'yarn install'
              }
            }
        }
        stage("build back") {
            steps {
              echo 'building the app with gradle'
                  sh 'mvn -v'
            }
        } 
        stage("test") {
            steps {
              echo 'testing the app'
            }
        }
        stage("deploy") {
            steps {
              echo 'deploying the app'
            }
        }
    }
}
