pipeline {
    agent {
        docker {
            image "maven:${MVN_VERSION}"
            args "-v $(which docker):/usr/bin/docker"
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
