pipeline {
    agent any
    tools { 
        maven "${MVN_VERSION}" 
    }
    stages {
        stage('Build') { 
            steps {
                sh 'mvn -B -DskipTests clean package' 
            }
        }
    }
}
