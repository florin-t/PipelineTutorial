pipeline {
    agent any
    stages {
        stage('Pre Build') {
            steps {
                sh 'echo "..."'
                sh '''
                    echo "Info about the system:"
                '''
                sh 'uname -a'

            }
        }
	stage('Build') {
            steps {
                sh 'echo "Hello There"'
                sh '''
                    echo "Multiline shell steps works too"
                '''
		sh 'ls -lah'
                
            }
        }
	stage('Post Build') {
            steps {
                sh 'echo "Bye"'
                sh '''
                    echo "last stage"
                   
                '''
	 	sh 'pwd'
            }
        }

    }
    stage('Test') {
            steps {
                sh 'echo "Fail!"; exit 1'
            }
    }

    post {
        always {
                echo 'This will always run'
        }
        success {
                echo 'This will run only if successful'
        }
        failure {
            echo 'This will run only if failed'
        }
        unstable {
            echo 'This will run only if the run was marked as unstable'
        }
        changed {
            echo 'This will run only if the state of the Pipeline has changed'
            echo 'For example, if the Pipeline was previously failing but is now successful'
        }
    }

}
