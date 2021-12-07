pipeline{
    agent{label 'master'}
    tools{maven 'M3'}
    stages{
        stage('Checkout'){
            steps{
                git branch: 'master', url: 'https://github.com/shiwaniraghav123/newcontactapp.git'
            }
        }
        stage('Build'){
            tools{
                jdk 'JAVA_HOME'
            }
            steps{
                bat 'mvn compile'
            }
        }
        stage('Package'){
            tools{
                jdk 'JAVA_HOME'
            }
            steps{
                bat 'mvn package'
            }
            }
        stage('Deploy'){
      steps{
 bat 'Java -jar C:\Users\MACHREDD\Downloads\contactapp\contactapp.jar'
         }
        }
    }
}
