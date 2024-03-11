pipeline {
    agent any
    
    stages {
        // stage('Clone repository') {
        //     steps {
        //         checkout([$class: 'GitSCM', 
        //         branches: [[name: '*/main']], 
        //         userRemoteConfigs: [[url: 'https://github.com/samarth-ramesh/PES2UG21CS465_jenkins.git']]])
        //     }
        // }
        
        stage('Build') {
            steps {
                build 'PES2UG21CS465_1'
                sh 'pwd; g++ ./main/main.cpp -o output'
            }
        }
        
        stage('Test') {
            steps {
                sh './output'
            }
        }
        
        stage('Deploy') {
            steps {
                echo 'deploy'
            }
        }
    }
    
    post {
        failure {
            error 'Pipeline failed'
        }
    }
}
