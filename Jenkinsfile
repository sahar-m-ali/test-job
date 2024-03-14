pipeline {
    agent any

    parameters {
     choice choices: ['DEV', 'QA', 'P PROD', 'PROD'], description: 'choose your env', name: 'ENVIRONMENT'
     string defaultValue: 'canary', description: 'choose the appropriate app', name: 'app'
     choice choices: ['ECR', 'DOKERHUB', 'NEXUS'], description: 'select the registry where you want to push your image', name: 'REGISTRY'
    }




    stages {
        stage('build') {
        when {
            expression {
            env.app == 'odilia'    //this will run if the cdt fits app equal to odilia

            }
        }
            steps {
                echo 'Hello World'
            }
        }



        stage('test') {
            when {
                expression {
                    env.REGISTRY == 'NEXUS' || env.REGISTRY == 'ECR' // this will work if the cdt fits  nexus or ecr
                }
            }
            steps {
                echo 'Hello World'
            }
        }


        stage('deploy') {
            when {
                expression {
                    env.ENVIRONMENT != 'DEV' // this will run if the cdt fits enironment not equal to dev
                }
            }
            steps {
                echo 'Hello World'
            }
        }

        stage('end') {
            when {
                expression {
                    env.ENVIRONMENT == 'DEV' && env.REGISTRY == 'ECR' // this 2 cdt should match for the end stage to be succes
                }
            }
            steps {
                echo 'Hello World'
            }
        }





    }





    
    









}
