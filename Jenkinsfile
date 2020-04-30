pipeline {
    agent any

    stages {
        stage ('Compile Stages') {

            steps {
                withMaven(maven : 'Maven3_5_4') {
                    sh 'mvn clean compile'
                }
            }
        }

        stage ('Testing Stages') {

            steps {
                withMaven(maven : 'Maven3_5_4') {
                    sh 'mvn test'
                }
            }
        }


        stage ('Deployment Stages') {
            steps {
                withMaven(maven : 'Maven3_5_4') {
                    sh 'mvn deploy'
                }
            }
        }
    }
}