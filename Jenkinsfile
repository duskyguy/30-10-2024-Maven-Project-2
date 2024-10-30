pipeline{
    agent any

    stages{

stage('test'){
            steps
            {   
                bat 'C:/Build/apache-maven-3.9.8/bin/mvn test'
            }
        }
stage('package'){
            steps
            {   
                bat 'C:/Build/apache-maven-3.9.8/bin/mvn package'
            }
        }
stage('install'){
            steps
            {   
                bat 'C:/Build/apache-maven-3.9.8/bin/mvn install'
            }
        }


    }
}
