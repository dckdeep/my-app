pipeline{
  agent any
  //stages {
  //stage('---clean---'){
    //steps{
     // sh "sudo rm -rf my-app"
      //sh "sudo mvn clean"
    //}
  //}
  stage('--test--'){
    steps {
      sh "sudo mvn test"
    }
  }
   stage ('Build') {
      steps {
         sh 'mvn -Dmaven.test.failure.ignore=true install' 
     }
    }
    
  stage('--package--'){
    steps{
      sh "sudo mvn package"
    }
  } 
  }
}
