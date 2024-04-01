# testrepo
To run some tests.

Jenkins job 
-----

name-test_job
#contents of the Execute Shell
java -version
echo "Welcome to jenkins"
chmod 777 /var/lib/jenkins/workspace/test_job/file1
sh /var/lib/jenkins/workspace/test_job/file1


Jenkins pipeline
-------------
name-test_job_pipeline
Option 1) pipeline script  

pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                echo "Welcome to jenkins"
                echo "Hello I'm using jenkinsfile"
                
            }
        }
    }
}


Option 2) pipeline script from SCM:Create a new jenkinsfile in repo and add below lines in it.

pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                echo "Welcome to jenkins"
                sh "chmod 777 file1"#we're giving the only filename because jenkins already has cloned the repo and kept it under the test_job_pipeline folder.#
                echo "changed permissions"
                 sh "./file1"
                
            }
        }
    }
}
