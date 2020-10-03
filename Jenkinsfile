pipeline{
    agent any

    environment {
        PASS = credentials('DOCKER_HUB_PASS')
        registryCredential = 'DOCKERHUB_ACCOUNT'

        DOCKER_IMAGE = 'phathdt379/cra'
    }

    stages{
        stage("build image docker"){
            steps {
                echo '****** Build and tag image docker nodejs******'

                sh './jenkins/build.sh'
            }
        }

        stage("push image"){
            steps{
                docker.withRegistry( '', registryCredential ) {
                    echo "====++++executing push image++++===="

                    sh "./jenkins/push.sh"
                }
            }
        }
    }
}
