pipeline {
    agent {docker docker-slave-fff0ddf0113d}

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
		singularity build hello-world.simg shub://vsoch/hello-world
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
