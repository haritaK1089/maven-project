pipeline {
    agent any
       tools{
      maven 'localMaven' 
 } 
   
stages{
        stage('Build'){
            steps {
                bat 'mvn clean package'
				bat ' docker build . -t Tomcat-webapp:${env.BUILD_ID}'
            }
            
        }
    }
}
