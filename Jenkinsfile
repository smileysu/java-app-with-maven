pipeline{
  agent any{
     stages{
       stage('git clone'){
        steps{ 
           git 'https://github.com/smileysu/java-app-with-maven.git'
        }
    }
  stage ('build the code'){
         steps{
            sh 'mvn package'
      }
    }
   stage('archive the artifacts'){
    steps{
      archive 'target/*.jar'   
}
}
stage('publish junit results'){
   steps{
    junit 'target/surefire-reports/*.xml'
     
    }
}
     }
  }
}
