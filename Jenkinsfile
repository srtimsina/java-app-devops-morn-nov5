pipeline {
    agent any

    stages {
        stage('Compile') {
            steps {
                echo 'Hello World'
                sh 'mvn clean package'
            }
        
       post { 
        success { 
            echo 'Archiving the artifact'
            archiveArtifacts artifacts: '**/*.war', followSymlinks: false
        }
    }
}
        stage('Build docker image') {
            steps {
                echo 'running unittest'
                sh 'docker build -t myregistry.local/myapp:"$BUILD_NUMBER"'
            }
        }
        stage('Createdockerimage') {
            steps {
                echo 'creating docker image'
            }
        }
    }
}

