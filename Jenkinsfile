pipeline {
    agent any
    parameters {
        choice(name: 'stage', choices:['Build', 'Test', 'Deploy', 'All'])
    }
    stages {
        stage('Build') {
            when {
                expression { ${env.stage} == 'All' || ${env.stage} == 'Build' }
            }
            steps {
                echo 'Building the application...'
            }
        }
        stage('Test') {
            when {
                expression { ${env.stage} == '' || ${env.stage} == 'Test' }
            }
            steps {
                echo 'Running tests...'
            }
        }
        stage('Deploy') {
            when {
                expression { ${env.stage} == '' || ${env.stage} == 'Deploy' }
            }
            steps {
                echo 'Deploying the application...'
            }
        }
    }
}
