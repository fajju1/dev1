env.mvnHome = '/usr/share/maven3'
node('mavenlable') {
   
   
   stage('Preparation') { // for display purposes
      
      git 'https://github.com/fajju1/dev1.git'
        
      
   }
   stage('Build') {
      
      if (isUnix()) {
         sh "'${mvnHome}/bin/mn' clean install"
      } else {
         bat(/"${mvnHome}\bin\mvn" -Dmaven.test.failure.ignore clean package/)
      }
   }
   stage('Results') {
      junit '**/target/surefire-reports/TEST-*.xml'
      archive 'target/*.jar'
   }
   stage('publish') {
     echo 'vdjhvbhjdsb'
   }
   

}
