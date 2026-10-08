pipeline {

    agent any

    tools {
        maven 'maven3'
    }

    stages {

        stage('Checkout') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/tanp4577-web/Maven-Package-Demo.git'
            }
        }

        stage('Package') {
            steps {
                bat 'mvn clean package'
            }
        }

        stage('Run JAR') {
            steps {
                bat 'java -cp target\\maven-package-demo-1.0.jar com.example.App'
            }
        }

    }
}
            
