pipeline {
    agent any
    parameters {
        choice(name: 'stage', choices:['Build', 'Test', 'Deploy', 'All'])
    }
    stages {
        stage('Build') {
            when {
                expression { params.stage == 'All' || params.stage == 'Build' }
            }
            steps {
                echo 'Building the application...'
            }
        }
        stage('Test') {
            when {
                expression { params.stage == 'All' || params.stage == 'Test' }
            }
            steps {
                echo 'Running tests...'
            }
        }
        stage('Deploy') {
            when {
                expression { params.stage == 'All' || params.stage == 'Deploy' }
            }
            steps {
                echo 'Deploying the application...'
            }
        }
    }
}
