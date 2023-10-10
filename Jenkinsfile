pipeline {
    agent {
        label 'dd'
    }


stages {
        stage('Compile Stage') {
            steps {
                script {
                    // Use 'sh' to run shell commands on a Linux agent
                    sh 'mvn clean compile'
                }
            }
        }

        stage('Testing Stage') {
            steps {
                script {
                    // Use 'sh' to run shell commands on a Linux agent
                    sh 'mvn test'
                }
            }
        }

        stage('Packaging Stage') {
            steps {
                script {
                    // Use 'sh' to run shell commands on a Linux agent
                    sh 'mvn package'
                }
            }
        }
    }
    }
