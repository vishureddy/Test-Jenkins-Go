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
                                sh "whoami" 
                                sh "sudo docker build . -t ${IMAGE_URL_WITH_TAG}"
                        }

                }
        }
}

def getDockerTag(){
    def tag  = sh script: 'git rev-parse HEAD', returnStdout: true
    return tag
}
