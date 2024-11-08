pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Clone the repository
                git branch: 'main', url: 'https://github.com/harshssn23/javaaa.git'
            }
        }

        stage('Compile') {
            steps {
                // Compile the Java program using 'javac'
                bat 'javac Test.java'
            }
        }

        stage('Run') {
            steps {
                // Run the compiled Java program
                bat 'java Test'
            }
        }
    }

    post {
        always {
            // Clean up the workspace
            cleanWs()
        }
        success {
            echo 'Java program executed successfully!'
        }
        failure {
            echo 'Execution of Java program failed.'
        }
    }
}
