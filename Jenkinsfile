pipeline {
    agent any
    stages {
        stage('Pre Build') {
            steps {
                sh 'echo "..."'
                sh '''
                    echo "Info about the system:"
                    uname -a
                '''
            }
        }
	stage('Build') {
            steps {
                sh 'echo "Hello There"'
                sh '''
                    echo "Multiline shell steps works too"
                    ls -lah
                '''
            }
        }
	stage('Post Build') {
            steps {
                sh 'echo "Bye"'
                sh '''
                    echo "last stage"
                    pwd 
                '''
            }
        }

    }
}
