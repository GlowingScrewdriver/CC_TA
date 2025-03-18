pipeline {
    agent any
    stages {
//        stage('Clone') {
//             steps {
//                 checkout([
//                     $class: "GitSCM",
//                     branches: [[name; "/main"]],
//                     userRemoteConfigs: [[url: "https://github.com/GlowingScrewdriver/CC_TA.git"]]
//                 ])
//             }
            stage('Build') {
                steps {
                    build 'PES1UG22SS682-1'
                    sh 'g++ some_program/hi.cpp -o some_program/hi'
                }
            }
            stage('Test') {
                steps {
                    sh 'some_program/hi'
                }
            }
            stage('Deploy') {
                steps {
                    echo 'Deploy (it seems)'
                }
            }
    }
    post {
        failure {
            error 'Pipeline failed'
        }
    }
}
