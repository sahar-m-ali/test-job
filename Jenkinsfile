pipeline {
    agent any

    parameters {
        choice choices: ['USA', 'Canada', 'Australia'], description: 'Choose your country.', name: 'COUNTRY'
        choice choices: ['ECR', 'Dockerhub'], description: 'Choose your registry', name: 'REGISTRY'
    }

    stages {
        stage('build') {
            steps {
                echo 'Hello World'
            }
        }


        stage('test') {
            steps {
                echo 'Hello World'
            }
        }

        stage('deploy') {
            steps {
                echo 'Hello World'
            }
        }

    
    }
}
