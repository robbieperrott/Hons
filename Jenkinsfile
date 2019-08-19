pipeline {
    agent any
    
    environment {
        SREGISTRY_CLIENT='registry'
        SREGISTRY_REGISTRY_BASE='http://nginx'
        SREGISTRY_REGISTRY_USERNAME='pianopwner'
        SREGISTRY_REGISTRY_TOKEN='0f92c8ab81ffa2929a3837b13578dffe49f81d47'
           
    }

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
