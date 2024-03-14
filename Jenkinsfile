pipeline {
    agent any
    stages {

        stage('pull') {
            steps {
                git branch: 'main', credentialsId: 'c7be23be-3d13-4287-84a9-b5967442e930', url: 'https://github.com/ashuvb17/Amazon-Jenkins.git'
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
                echo 'sucsess in build'
            }
        }

    }

  post{
    
  failure{
       echo 'Failure in the build'
   }

  }


}
