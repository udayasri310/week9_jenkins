pipeline {
    agent any
    tools{
        maven 'MAVEN-HOME'
    }
    stages {
        stage('git repo & clean') {
            steps {
                //bat "rmdir  /s /q mavenjava"
                bat "git clone provide your github link"
                bat "mvn clean -f mavenjava"
            }
        }
        stage('install') {
            steps {
                bat "mvn install -f my-maven-project" #project name#
            }
        }
        stage('test') {
            steps {
                bat "mvn test -f my-maven-project"
            }
        }
        stage('package') {
            steps {
                bat "mvn package -f my-maven-project"
            }
        }
    }
}