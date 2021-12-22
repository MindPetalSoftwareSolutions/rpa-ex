@Library('jenkins-shared-library@Justin-dev') _

pipeline {
    agent any
    stages {
        stage('Sonar') {
            steps {
                sonarQubeScan()
            }
        }
        stage('Pack and Publish') {
            steps {
                script {
                    orchPublish("default", "VerticalApps") 
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
