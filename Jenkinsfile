pipeline {
    agent any
    triggers { pollSCM ('5 * * * *') }
     stages {
        stage('shop') {
            steps { 
                git branch: 'develop' ,
                  url:'https://github.com/madhu0018/shopizer.git' 
                }
        }
        stage ( 'package' ) {
            steps {
                sh 'mvn package'
            }
        }
   }
}