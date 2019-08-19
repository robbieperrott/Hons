pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                singularity build test.simg Singularity.recipe
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
