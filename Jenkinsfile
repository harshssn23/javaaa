pipeline {
    agent any  // This specifies any available Jenkins agent
    
    stages {
        stage('Checkout') {
            steps {
                // Clone the repository containing the Java file
                git branch: 'main', url: 'https://github.com/harshssn23/javaaa.git' // Replace with your Git repo URL
            }
        }

        stage('Compile') {
            steps {
                // Compile the Java file
                script {
                    sh 'javac Test.java'
                }
            }
        }

        stage('Run') {
            steps {
                // Run the Java program
                script {
                    sh 'java Test'
                }
            }
        }
    }

    post {
        always {
            // Cleanup workspace
            cleanWs()
        }
        success {
            // Print success message
            echo 'Java program executed successfully!'
        }
        failure {
            // Print failure message
            echo 'Execution of Java program failed.'
        }
    }
}
