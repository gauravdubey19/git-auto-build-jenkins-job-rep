pipeline {
    agent any

    stages {

        stage('Show Commit ID') {
            steps {
                script {
                    if (isUnix()) {
                        sh 'echo "Git Commit ID: $(git rev-parse HEAD)"'
                    } else {
                        bat 'echo Git Commit ID:'
                        bat 'git rev-parse HEAD'
                    }
                }
            }
        }

        stage('Compile Java') {
            steps {
                script {
                    if (isUnix()) {
                        sh 'javac HelloMaam.java'
                    } else {
                        bat 'javac HelloMaam.java'
                    }
                }
            }
        }

        stage('Run Java Program') {
            steps {
                script {
                    if (isUnix()) {
                        sh 'java Hello'
                    } else {
                        bat 'java Hello'
                    }
                }
            }
        }
    }
}
