pipeline {
    agent any

    stages {
        stage('Compile') {
            steps {
                echo 'Hello World'
                sh 'mvn clean package'
            }
        }
       post { 
        success { 
            echo 'Archiving the artifact'
            archiveArtifacts artifacts: '**/*.war', followSymlinks: false
        }
    }
        stage('Unittest') {
            steps {
                echo 'running unittest'
            }
        }
        stage('Createdockerimage') {
            steps {
                echo 'creating docker image'
            }
        }
    }
}

