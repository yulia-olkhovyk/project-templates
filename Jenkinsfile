#!groovy
// Check ub1 properties
properties([disableConcurrentBuilds()])

pipeline {
    agent { 
        label 'master'
        }
    options {
        buildDiscarder(logRotator(numToKeepStr: '10', artifactNumToKeepStr: '10'))
        timestamps()
    }
    stages {
        stage("First step") {
            steps {
                sh 'ssh root@jenkins-agent-alma \'hostname\''
            }
        }
        stage("Second step") {
            steps {
                sh 'ssh root@jenkins-agent-alma1 \'uptime\''
            }
        }
    }
}