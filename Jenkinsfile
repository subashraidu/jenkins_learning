pipeline {
    agent any

    tools {
        maven 'mymaven'
    }

    stages {
        stage('Checkout the Code') {
            steps {
                git 'https://github.com/subashraidu/DevOpsCodeDemo.git'
            }
        }

        stage('Code Review') {
            steps {
                sh 'mvn pmd:pmd'
            }
        }

        stage('Compile the Code') {
            steps {
                sh 'mvn compile'
            }
        }

        stage('Test the Code') {      
            steps {
                sh 'mvn test'
            }
        }

        stage('Package the Code') {
            steps {
                sh 'mvn package'
            }
        }
    }
}
