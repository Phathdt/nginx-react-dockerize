pipeline{
    agent any

    environment {
        DOCKER_IMAGE = 'phathdt379/cra'
    }

    stages{
        stage("build image docker"){
            steps {
                echo '****** Build and tag image docker nodejs******'

                sh './jenkins/build.sh'
            }
        }
    }
}
