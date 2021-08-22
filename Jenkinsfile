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
                #'-P metrics pmd:pmd --reportfile **/*.xml --exclude vendor/ || exit 0'
                #pmd canRunOnFailed: true, pattern: '**/*.xml'
            }
        }

        
        
        stage ('package'){
            steps {
                echo "Building war file"
                sh 'mvn package'
                #archiveArtifacts artifacts : 'target/*.war'
            }
        }

    }
}
