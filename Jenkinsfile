pipeline {
    agent any
    tools {
        maven 'MAVEN_HOME' // must match your Jenkins Maven installation name
    }
    stages {
        stage('git repo & clean') {
            steps {
                // Clone the repo
                bat "git clone https://github.com/udayasri310/week9_jenkins.git"
                // Change directory into the repo and run maven clean
                dir('week9_jenkins') {
                    bat "mvn clean"
                }
            }
        }
        stage('install') {
            steps {
                dir('week9_jenkins') {
                    bat "mvn install"
                }
            }
        }
        stage('test') {
            steps {
                dir('week9_jenkins') {
                    bat "mvn test"
                }
            }
        }
        stage('package') {
            steps {
                dir('week9_jenkins') {
                    bat "mvn package"
                }
            }
        }
    }
}
