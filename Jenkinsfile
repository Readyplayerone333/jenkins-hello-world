pipeline {
    agent any

    tools {
        maven "M398"
    }

    stages {
        stage("Echo version") {
            steps {
                sh 'echo maven version'
                sh 'mvn --version'
                }
            }
        stage('Build'){
            steps{
                //git branch: 'main', url: 'https://github.com/Readyplayerone333/jenkins-hello-world.git'
                sh 'mvn clean package -DskipTests=true'
            }
        
        }
        stage('Test'){
            steps{
                sh 'mvn test'
            }
        }
    }
}
