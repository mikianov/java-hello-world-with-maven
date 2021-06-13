pipeline {
    agent {
        docker {
          image "maven:${MVN_VERSION}"
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
