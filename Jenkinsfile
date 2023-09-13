pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                // Your build steps here (if needed)
            }
        }
        stage('Run Demo1') {
            steps {
                sh 'python demo1.py'
            }
        }
        stage('Run Demo2') {
            steps {
                sh 'python demo2.py'
            }
        }
    }
}
