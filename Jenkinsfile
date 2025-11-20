pipeline {
    agent any
    tools {
        gradle 'Gradle9'   // matches the name you configured
    }
    stages {
        // stage('Checkout') {
        //     steps {
        //         checkout scm
        //     }
        // }
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
