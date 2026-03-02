pipeline {
    agent any

    tools {
        jdk 'JDK'   // Must match name in Jenkins Global Tool Config
    }

    stages {

        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/LikithReddy0409/2023MyGradle.git'
            }
        }

        stage('Build') {
            steps {
                sh './gradlew clean build'
            }
        }

    }

    post {
        success {
            echo 'Build successful!'
        }
        failure {
            echo 'Build failed!'
        }
    }
}
