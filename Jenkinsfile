pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'g++ -c PES1UG20CS625.cpp'
                sh 'g++ -o PES1UG20CS25 PES1UG20CS625.cpp'
                echo 'Build successful'
            }
        }
        stage('Test') {
            steps {
                sh 'PES1UG20CS625'
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
    }
}
