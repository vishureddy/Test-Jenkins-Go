pipeline{
        agent any
        environment{
        DOCKER_TAG=getDockerTag()
        }


        stages{
                stage('build Docker Image'){
                        steps{
                                sh "docker build -t localhost:5000/nodeapp:${DOCKER_TAG}"
                        }
                }
        }
}

def getDockerTag(){
        def tag = sh script: "git rev-parse HEAD", returnStdout:true
        return tag
}

