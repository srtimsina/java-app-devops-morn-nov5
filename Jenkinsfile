pipeline {
    agent any

    stages {
        stage('Compile') {
            steps {
                echo 'Hello World'
                sh 'mvn clean package'
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

