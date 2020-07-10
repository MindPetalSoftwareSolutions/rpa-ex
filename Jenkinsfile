@Library('jenkins-modern-folder-shared-library@master') _

pipeline {
    agent any
    stages {
        /*stage('Sonar') {
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
        stage('Post-Build') {
            steps {
                postBuild()
            }
        }
    }
}
