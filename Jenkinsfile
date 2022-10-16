pipeline {
    agent any
    triggers { cron ('* 18 * * *') }
     stages {
        stage('shop') {
            steps { 
                git branch: 'Releas' ,
                  url:'https://github.com/madhu0018/shopizer.git' 
                }
        }
        stage ( 'package' ) {
            steps {
                sh 'mvn package'
                 }
        }
        stage('archive artifacts') {
            steps {
            archive includes: "**/target/*.jar"
       } 
        }
        stage('junit test results') {
            steps {
                junit testResults: "**/target/surefire-reports/*.xml"
            }
        }
     }
}