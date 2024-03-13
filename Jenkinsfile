pipeline {
    agent any
    stages {

        stage('pull') {
            steps {
                git branch: 'main', url: 'https://github.com/ashuvb17/Amazon-Jenkins.git'
            }
        }

        stage('compile') {
            steps {
                sh 'mvn compile'
            }
        }

        
        stage('build') {
            steps {
                 sh 'mvn clean install'
            }
        }

    }

  post{
    
  failure{
       echo 'Failure in the build'
   }

  }


}
