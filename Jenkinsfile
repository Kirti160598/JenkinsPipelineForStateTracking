pipeline {
    agent any
    
    environment {
        LAST_SUCCESS_STEP = readFile('last_step.txt').trim()
    }
    
    stages {
        stage('Step 1') {
            when {
                expression { LAST_SUCCESS_STEP != 'Step 1' }
            }
            steps {
                echo 'Executing Step 1'
                writeFile file: 'last_step.txt', text: 'Step 1'
            }
        }
        
        stage('Step 2') {
            when {
                expression { LAST_SUCCESS_STEP != 'Step 2' }
            }
            steps {
                echo 'Executing Step 2'
                script {
                    if (sh(script: 'exit 1', returnStatus: true) != 0) {
                        error('Step 2 Failed!')
                    }
                }
                writeFile file: 'last_step.txt', text: 'Step 2'
            }
        }
        
        stage('Step 3') {
            when {
                expression { LAST_SUCCESS_STEP != 'Step 3' }
            }
            steps {
                echo 'Executing Step 3'
                writeFile file: 'last_step.txt', text: 'Step 3'
            }
        }
        
        stage('Step 4') {
            when {
                expression { LAST_SUCCESS_STEP != 'Step 4' }
            }
            steps {
                echo 'Executing Step 4'
                writeFile file: 'last_step.txt', text: 'Step 4'
            }
        }
    }
}
