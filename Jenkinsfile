pipeline {
    agent {
        label 'dd'
    }


stages {
        stage('Set Git Version') {
            steps {
                script {
                    // Set the Git version in the PATH environment variable
                    withEnv(["PATH=/path/to/git-2.34.1/bin:$env.PATH"]) {
                        // Now, the pipeline will use Git version 2.34.1
                        // Your Git-related steps go here
                        sh 'git --version' // Example: Check Git version
                    }
                }
            }
        }

        stage('Compile Stage') {
            steps {
                script {
                    // Your compile steps here
                }
            }
        }

        stage('Testing Stage') {
            steps {
                script {
                    // Your testing steps here
                }
            }
        }

        stage('Packaging Stage') {
            steps {
                script {
                    // Your packaging steps here
                }
            }
        }
    }
    }
