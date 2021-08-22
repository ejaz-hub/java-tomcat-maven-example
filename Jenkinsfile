pipeline {
    agent any

    stages {
        stage ('Build') {
            steps {
                sh 'mvn compile'
            }
        }

        stage ('Test') {
            steps {
                sh echo "Testing the code"
                'mvn test'
            }
        }

        
        
        stage ('package'){
            steps {
                echo "Building war file"
                sh 'mvn package'
        }

    }
}
}
