pipeline {
   agent any
   tools {
      maven "maven"
   }
   stages {
      stage('checkout') {
         steps {
            git 'https://github.com/kliakos/sparkjava-war-example.git'
         }
      }
      stage('Build') {
         steps {
            sh "mvn clean install package"
         }
      }
      stage('deploy') {
         steps {
            sh 'sh /opt/deploy.sh'
         }
      }
      
       
   }
}  
