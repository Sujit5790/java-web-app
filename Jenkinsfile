pipeline{
    agent any
     stages{
        stage('checkout code'){
            steps{
                git branch: 'main', url:'https://github.com/Sujit5790/java-web-app.git'
            }

        }
        stage('build code'){
            steps{
                sh 'mvn clean package'
            }
            
        }
        stage('deploy to tomcat'){
            steps{
                deploy adapters:[tomcat9:(url:'http://43.204.101.236:8080', credentialsId:'tomcatcred')], war:'**'
            }

        }
     }
}