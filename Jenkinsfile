pipeline {
    agent any

    stages {
        stage ('Compile Stage') {
            steps {
                withMaven() {
                    sh 'mvn --version'
                    sh 'mvn clean compile'
                }
            }
        }

        stage ('Testing Stage') {

            steps {
                withMaven() {
                    sh 'mvn test'
                }
            }
        }


        stage ('Deployment Stage') {
            steps {
                withMaven() {
                    sh 'mvn deploy'
                }
            }
        }
    }
}
