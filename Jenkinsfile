pipeline {
    agent any

    tools {
        // Specify the Maven tool installation (use 'Maven' on Linux agents)
        maven "Maven"
    }

    stages {
        stage('Compile Stage') {
            steps {
                // Use 'sh' to run shell commands on a Linux agent
                withMaven(
                    maven: 'Maven', // Use 'Maven' tool installation
                    mavenLocalRepo: '.repository' // Optional local repository location
                ) {
                    sh 'mvn clean compile'
                }
            }
        }

        stage('Testing Stage') {
            steps {
                withMaven(
                    maven: 'Maven', // Use 'Maven' tool installation
                    mavenLocalRepo: '.repository' // Optional local repository location
                ) {
                    sh 'mvn test'
                }
            }
        }

        stage('Packaging Stage') {
            steps {
                withMaven(
                    maven: 'Maven', // Use 'Maven' tool installation
                    mavenLocalRepo: '.repository' // Optional local repository location
                ) {
                    sh 'mvn package'
                }
            }
        }
    }
}
