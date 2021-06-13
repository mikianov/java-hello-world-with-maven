pipeline {
    agent {
        docker {
            image "maven:${MVN_VERSION}"
            args "-v /var/run/docker.sock:/var/run/docker.sock -v \$(which docker):\$(which docker)"
        }
    }
    stages {
        stage('Build') { 
            steps {
                sh 'mvn -B -DskipTests clean package' 
            }
        }
    }
}
