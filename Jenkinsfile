pipeline {
    agent {
        docker {
            image "maven:${MVN_VERSION}"
            args "-v $(which docker):/usr/bin/docker"
        }
    }
    
pipeline {
    agent {
        docker { image 'node:14-alpine' }
    }
    stages {
        stage('Build') { 
            steps {
                sh 'mvn -B -DskipTests clean package' 
            }
        }
    }
}
