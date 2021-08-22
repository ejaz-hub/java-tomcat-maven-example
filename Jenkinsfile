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
                sh '''
                      #!/bin/bash
                      echo "Testing the code"
                      mvn test'''
            }
        }

        
        
        stage ('package'){
            steps {
                sh'''
                    #!/bin/bash
                    echo "Testing the code"
                    mvn test'''
        }

    }
}
}
