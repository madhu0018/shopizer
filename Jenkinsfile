pepeline {
    agent {labe 'SHOPIZER'}

     stages {
        stage('shop') {
            steps { 
                git branch: 'master' url:'https://github.com/madhu0018/shopizer1.git' 
                }

        }
     }
        stage ('package') {
            steps {
                sh 'mvn package'
            }
        }

}