pipeline {
    agent any
    tools { 
        maven "Maven ${MVN_VERSION}" 
    }
    stages {
        stage('Build') { 
            steps {
                sh 'mvn -B -DskipTests clean package' 
            }
        }
    }
}
