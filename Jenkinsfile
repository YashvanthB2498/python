pipeline {
    agent any
    
    stages {
       steps {
        // Replace these commands with your actual build commands
        sh 'make clean'
        sh 'make'
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
