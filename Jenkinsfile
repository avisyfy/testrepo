pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                echo "Welcome to jenkins"
                sh "chmod 777 file2.sh"
                echo "changed permissions"
                 sh "./file2.sh"
                
            }
        }
    }
}
