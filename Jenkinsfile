pipeline {
    agent any
    tools {
        maven 'Maven3_5_4'
    }

    stages {
        stage ('Compile Stage') {

            steps {
                    sh 'mvn -B -DskipTests clean package'
                  }
        }

        stage ('Testing Stage') {
            steps {
                    sh 'mvn test'
                  }
        }


        stage ('Deployment Stage') {
            steps {
                    sh 'mvn deploy'
                  }
        }
    }
}