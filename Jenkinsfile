pipeline{
    agent any
    stages{
        stage("build image docker"){
            steps {
                echo '****** Build and tag image docker nodejs******'

                sh './jenkins/build.sh'
            }
        }
    }
}
