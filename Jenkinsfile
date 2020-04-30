pipeline {
    agent any
    tools {
        maven 'apache-maven-3.5.4'
    }

    stages {
        stage ('Compile Stage') {

            steps {
                    sh 'mvn --version'
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