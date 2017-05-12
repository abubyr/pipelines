#!groovy
def CONT_NAME = "showuname"
pipeline {
    agent any
    stages {
        stage('Show uname docker') {
            steps {
                def dockerApp = docker.image('ubuntu:latest')
                dockerApp.pull()
                dockerApp.inside {
                    sh "/bin/uname -a"
                }
            }
        } // stage section
    } // stages section
    /*post {
        always {
            sh "/usr/bin/docker stop ${CONT_NAME}"
            sh "/usr/bin/docker rm -f ${CONT_NAME}"
        }
    }*/
}
