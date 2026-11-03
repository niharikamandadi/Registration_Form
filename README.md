A modern, responsive web-based user management system for registering, viewing, searching, editing, and deleting user records - built with simplicity, usability, and client-side persistence in mind.


pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                git(
                    url: 'https://github.com/niharikamandadi/jenkins.git',
                    branch: 'main'
                )
            }
        }

        stage('Build') {
            steps {
                echo 'Building Registration Form Project'

                sh 'ls -la'

                sh 'test -f index.html'
                sh 'test -f display.html'

                echo 'Build completed successfully'
            }
        }
    }
}
