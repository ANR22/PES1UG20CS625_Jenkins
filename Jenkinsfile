pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'g++ -c newcpp.cpp'
                sh 'g++ -o newcpp newcpp.cpp'
                echo 'Build successful'
            }
        }
        stage('Test') {
            steps {
                sh './newcpp'
                echo 'Test was successful'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploy steps successful'
            }
        }
        
    }
  post{
    failure{
      echo 'Pipelined failed'
}
