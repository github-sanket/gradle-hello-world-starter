pipeline {
    agent any

    tools {
        gradle 'gradle-9.2.1'   // name you configured in Jenkins
    }

    stages {
         stage('Checkout') {
             steps {
                 checkout scm
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
