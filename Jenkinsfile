@Library('jenkins-modern-folder-shared-library@Justin-dev') _

pipeline {
    agent any
    stages {
       /* stage('Sonar') {
            steps {
                sonarQubeScan()
            }
        }*/
        stage('Pack and Publish') {
            steps {
                script {
                  orchPublish("default", "VerticalApps") 
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