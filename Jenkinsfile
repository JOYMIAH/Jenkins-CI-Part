pipeline{
    agent any
    envirorment{
        DOCKERHUB_USERNAME="joymiah"
        APP_NAME="todo-app-joy"
        IMAGE_TAG="${BUILD_NUMBER}"
        IMAGE_NAME="${DOCKERHUB_USERNAME}" + "/" + "${APP_NAME}"
        REGISTRY_CREDS= 'dockerhub'
    }

    stages{

        stage('CleanUp The Workspace'){

            step{
                script{
                    cleanWs()
                }
            }
        }
        stage('Checkout Source Code Management'{
            steps{
                script{
                    git credentialsId: 'github',
                    url: 'https://github.com/JOYMIAH/Jenkins-CI-Part.git',
                    branch: 'main'


                }
            }
        })
            
        }

    }



