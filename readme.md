# rpa-ex
Example git repository

# Step 1: Add Jenkinsfile to your GitHub Repository

## Jenkinsfile breakdown

### Library tag which specifies which library in Jenkins to use. Do not change

```
@Library('jenkins-modern-folder-shared-library@master') _
```

### Pipeline delcaration and agent specification. Do not change
```
pipeline {
    agent any
```

### Pipeline stage: Sonar: Specifies that the source code should be scanned by SonarQube. Do not change

```
    stages {
        stage('Sonar') {
            steps {
                sonarQubeScan()
            }
        }
```
### Pipeline stage: Pack and Publish: First string "Default" specifies the tenant. Should be updated to correct tenant name for Orchestrator instance. Second string "PAER" specifies the folder where process will be published. Should be updated to proper folder name by developer.
```
        stage('Pack and Publish') {
            steps {
                script {
                    orchPublish("Default", "PAER") 
                }
            }
        }
```
### Pipeline stage: Post-Buid: Cleans up Jenkins working directory. Do not change.
```
        stage('Post-Build') {
            steps {
                postBuild()
            }
        }
    }
}
```

# Step 2: Configure Jenkins to execute builds

## Jenkins configuration

### Create a pipeline job
![Create a Pipeline Job](https://github.com/VerticalApps-DevOps/rpa-resources/blob/master/create_job.png)

### Job Detials
![Job Details](https://github.com/VerticalApps-DevOps/rpa-resources/blob/master/job_details.png)

Now you are ready to execute your builds!
