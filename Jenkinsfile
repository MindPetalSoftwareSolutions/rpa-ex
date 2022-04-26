@Library('jenkins-modern-folder-shared-library@sbom') _

pipeline {
    agent any
    stages {
        stage('SBoM') {
            steps {
                generateSBoM()
            }
        }
    }
}
