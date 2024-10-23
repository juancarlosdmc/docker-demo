pipeline {
    agent any

    tools {
        gradle 'Gradle'    
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
                  sh './gradlew -v'
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
