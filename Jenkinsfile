pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                sh 'singularity build test.simg Singularity.recipe'
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
                sh 'export SREGISTRY_CLIENT=registry'
                sh 'sregistry push test.simg --name=test/jenkinstest'
            }
        }
    }
}
