pipeline {
    agent {
        docker {
            image 'maven:3.9.2-eclipse-temurin-8-alpine' 
            args '-v /root/.m2:/root/.m2' 
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