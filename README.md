# jkpractical
Jenkins CI test
pipeline {
    agent any

    stages {
        stage('Checkout Code') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/Abhi00kh/jkpractical.git'
            }
        }

        stage('Build') {
            steps {
                echo 'Build started'
                bat 'dir'
                echo 'Build completed successfully'
            }
        }
    }
}
