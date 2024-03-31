pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                echo "Welcome to jenkins"
                sh "chmod 777 /var/lib/jenkins/workspace/test_job_pipeline/file1"
                echo "changed permissions"
                 sh "/var/lib/jenkins/workspace/test_job_pipeline/file1"
                
            }
        }
    }
}
