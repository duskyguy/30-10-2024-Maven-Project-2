pipeline {
  agent any
  triggers {
    pollSCM('*/5 * * * *')
  }
  stages{
       stage ('Build'){
        steps {
                bat 'C:/Build/apache-maven-3.9.8/bin/mvn build'

        }
       /*  post {
           success {
             echo 'Archiving...'
             archiveArtifacts artifacts:'**/target/*.war'
           }
         }
       }
       stage ('Deployments') {
         parallel{
           stage ('Deploy to Staging'){
             steps {
               sh "cp **/target/*.war /home/ivan/programms/tomcat-staging/webapps"
             }
           }
           stage ('Deploy to prod') {
             steps {
               sh "cp **/target/*.war /home/ivan/programms/tomcat-prod/webapps"
             }     
           }
         }*/
       }
    }
} 
  
