pipeline {
    agent any

    stages {
        stage('Clone Remote Repository') {
            steps {
                // Clone the remote Git repository
                checkout([$class: 'GitSCM',
                          branches: [[name: '*/main']],
                          doGenerateSubmoduleConfigurations: false,
                          extensions: [[$class: 'GitUsernamePasswordAuthentication',
                                        credentialsId: 'Git_credentials']],
                          userRemoteConfigs: [[url: 'https://code.fresco.me/Hackathon/internal-recruitment/pluseval-jenkins-declarativepipeline.git']]])
            }
        }

        stage('Run Python Scripts') {
            steps {
                // Change to the directory with Python scripts
                dir('*/main') {
                    sh 'python demo1.py'
                    sh 'python demo2.py'
                }
            }
        }
    }
}
