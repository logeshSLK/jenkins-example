pipeline {
    agent any
    
    environment {
    PATH ="/opt/maven3/bin:$PATH"
    }
    
    stages {
        stage ('Compile Stage') {

            steps {
                withMaven(maven : 'maven3') {
                    sh 'mvn clean compile'
                }
            }
        }

        stage ('Testing Stage') {

            steps {
                withMaven(maven : 'maven3') {
                    sh 'mvn test'
                }
            }
        }


        stage ('Deployment Stage') {
            steps {
                withMaven(maven : 'maven3') {
                    sh 'mvn deploy'
                }
            }
        }
    }
}
