pipeline {
    agent any
    stages {
        stage('Build') {
            when {
                expression {
                    // Run only if state is missing or before 'build'
                    !fileExists('pipeline_state.txt') ||
                    readFile('pipeline_state.txt').trim() == 'start'
                }
            }
            steps {
                script {
                    echo "Running Build Stage..."
                    // Simulate work
                    sh 'echo build > output.txt'
                    // Save state
                    writeFile file: 'pipeline_state.txt', text: 'build'
                }
            }
        }

        stage('Test') {
            when {
                expression {
                    fileExists('pipeline_state.txt') &&
                    readFile('pipeline_state.txt').trim() == 'build'
                }
            }
            steps {
                script {
                    echo "Running Test Stage..."
                    sh 'cat output.txt'
                    writeFile file: 'pipeline_state.txt', text: 'test'
                }
            }
        }

        stage('Deploy') {
            when {
                expression {
                    fileExists('pipeline_state.txt') &&
                    readFile('pipeline_state.txt').trim() == 'test'
                }
            }
            steps {
                script {
                    echo "Running Deploy Stage..."
                    writeFile file: 'pipeline_state.txt', text: 'done'
                }
            }
        }

        stage('Done') {
            when {
                expression {
                    fileExists('pipeline_state.txt') &&
                    readFile('pipeline_state.txt').trim() == 'done'
                }
            }
            steps {
                echo "Pipeline already completed."
            }
        }
    }
}
