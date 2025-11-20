pipeline {
    agent any
    tools {
        jdk 'jdk-21'   // matches the name you configured
    }
    stages {
        // stage('Checkout') {
        //     steps {
        //         checkout scm
        //     }
        // }
        stage('Debug Java') {
            steps {
                sh 'java -version'
                sh 'echo $JAVA_HOME'
            }
        }
        stage('Gradle Build') {
            steps {
                sh './gradlew clean build'
            }
        }
        // stage('Test') {
        //     steps {
        //         sh './gradlew test'
        //     }
        // }
    }
    post {
        success {
            echo "Build completed successfully!"
        }
        failure {
            echo "Build failed!"
        }
    }
}
