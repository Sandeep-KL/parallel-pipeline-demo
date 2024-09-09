pipeline {
    agent none

    stages {
        stage('Build and run') {
          parallel {
            stage('master-agent-pipeline') {
              agent {label 'master'}
              stages{
                stage('Build') {
                steps {
                  echo 'Building..'
                  }
                }
                stage('Test') {
                  steps {
                    echo 'Testing..'
                 }
                }
	       }
              }
            stage('label1-agent-pipeline') {
              agent {label 'label1'}
              stages{
                stage('Build') {
                steps {
                  echo 'Building..'
                  }
                }
                stage('Test') {
                  steps {
                    echo 'Testing..'
                 }
                }
               }
              }
             }
            }
           }
          }
