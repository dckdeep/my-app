pipeline {
    agent any 
    stages {
        stage('clone repo and clean ') { 
            steps {
                sh "sudo rm -rf my-app"
                sh "sudo git clone https://github.com/dckdeep/Delhi-Diamond.git"
                sh "sudo mvn clean -f my-app"
            }
        }
        stage('Test') { 
            steps {
                sh "sudo mvn test -f my-app" 
            }
        }
        stage('Deploy') { 
            steps {
                sh "sudo mvn package -f my-app" 
            }
        }
    }
}
