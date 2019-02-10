pipeline {
    agent any
    stages {
        stage('---clean---') {
def mvn_version = 'maven 3.6.0'
        withEnv( ["PATH+MAVEN=${tool mvn_version}/bin"] )
            steps {
                sh "mvn clean"
            }
        }
        stage('--test--') {
            steps {
                sh "mvn test"
            }
        }
        stage('--package--') {
            steps {
                sh "mvn package"
            }
        }
    }
}