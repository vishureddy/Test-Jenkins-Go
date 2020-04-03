pipeline{
        agent any
        environment{
                DOCKER_TAG = getDockerTag()
                DOCKER_REGISTRY_URL  = "127.0.0.0:8080"
                IMAGE_URL_WITH_TAG = "${DOCKER_REGISTRY_URL}/node-app:${DOCKER_TAG}"
        }
        stages{
                stage('Buid Docker Image'){
                        steps{
<<<<<<< HEAD
                                sh "docker build . -t ${IMAGE_URL_WITH_TAG}"
=======
                                sh "docker build -t localhost:5000/nodeapp:${DOCKER_TAG} ."
>>>>>>> 24af2c95ea174c4f2bbe1f22ba71a6e9d731e7e0
                        }

                }
        }
}

def getDockerTag(){
    def tag  = sh script: 'git rev-parse HEAD', returnStdout: true
    return tag
}
