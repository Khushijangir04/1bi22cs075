pipeline{
  agent any
   tools{
     maven 'Maven'
   }
   stages{
    stage('Checkout'){
      step{
        git branch: 'master', url https://github.com/Khushijangir04/1bi22cs075.git
      }
  }
  stage('Build'){
    step{
       sh 'mvn clean package'
    }
  }
  stage ('Test'){
   step{
     sh 'mvn test'
    }
   }
  stage('Run'){
     step{
       sh 'java -jar target/1bi22cs075-1.0-SNAPSHOT'
     }
  }
 }
 post{
  success{
    echo 'Build Successful'
   }
  failure{
    echo 'Build failed'
   }
 }
}
