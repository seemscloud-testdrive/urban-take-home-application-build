pipeline {
    agent any
    stages {
        stage('Create'){
            parallel {
                stage('First') {
                    agent {
                        docker {
                            image 'alpine:3.13.6'
                        }
                    }
                    steps {
                        git branch: 'main', credentialsId: 'df6af479-0544-4b53-8659-0d1ffc194302', url: 'git@github.com:seemscloud-testdrive/urban-take-home-application.git'
                        sh 'ls -lh'
                    }
                }
            }   
        }
    }
}
