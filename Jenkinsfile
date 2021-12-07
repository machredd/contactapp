pipeline{
    agent{label 'master'}
    tools{maven 'M3'}
    stages{
        stage('Checkout'){
            steps{
                git branch: 'master', url: 'https://github.com/machredd/contactapp.git'
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
  bat 'Java -jar C:/Program Files (x86)/Jenkins/workspace/contactapppipeline/target/contact-application-spring-0.0.1-SNAPSHOT.jar'
         }
        }
    }
}
