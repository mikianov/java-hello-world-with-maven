pipeline {
    agent any
    tools { 
        maven "${MVN_VERSION}" 
    }
    stages {
        stage('Build') { 
            steps {
                sh "mvn -B -DskipTests versions:set -DnewVersion=${JAVA_DEFAULT_VERSION} clean package"
            }
        }
    }
}
