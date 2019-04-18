pipeline {
    agent any

    stages {
        stage('Compile Stage') {
            steps {
               withMaven(maven : 'maven-2.2.1'){
                 sh 'mvn clean compile'
                 }
            }
        }
        stage('Testing stage') {
            steps {
               withMaven(maven : 'maven-2.2.1'){
                 sh 'mvn test'
                 }
            }
        }
        stage('Deploy') {
            steps {
               (withMavenmaven : 'maven-2.2.1'){
                 sh 'mvn deploy'
                 }
            }
        }
    }
}
