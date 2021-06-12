@Library('jenkins-modern-folder-shared-library@modular') _

pipeline {
    agent any
    /*
    stages {
        stage('Sonar') {
            steps {
                sonarQubeScan()
            }
        }*/
        stage('Pack and Publish') {
            steps {
                script {
                  orchPublish("Default", "PAER") 
                }
            }
        }
    }
    post {
        always {
            postBuild()
        }
    }
}
