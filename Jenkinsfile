@Library('jenkins-shared-library@Justin-dev') _

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
                    orchPublish("VerticalApps", "Test") 
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
