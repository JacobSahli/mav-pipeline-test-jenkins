pipeline {
    agent any


    stages {
        stage('Compile Stage') {
            steps {
                // Use 'sh' to run shell commands on a Linux agent

                    sh 'mvn clean compile'
                
            }
        }

        stage('Testing Stage') {
            steps {

                    sh 'mvn test'

            }
        }

        stage('Packaging Stage') {
            steps {

                    sh 'mvn package'
}
            }
        }
    }
