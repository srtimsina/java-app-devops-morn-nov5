pipeline {
    agent any

    stages {
        stage('Compile') {
            steps {
                echo 'Hello World'
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

