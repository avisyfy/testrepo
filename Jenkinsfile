pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                echo "Welcome to jenkins"
                chmod 777 /var/lib/jenkins/workspace/test_job/file1
                echo "changed permissions"
                 sh /var/lib/jenkins/workspace/test_job/file1
                
            }
        }
    }
}
