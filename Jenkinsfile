pipeline {
    agent any

    stages {
        stage('Step 1') {
            when { 
                expression { fileExists('last_step.txt') && readFile('last_step.txt').trim() != 'Step 1' }
            }
            steps {
                echo 'Executing Step 1 print step1'
                writeFile file: 'last_step.txt', text: 'Step 1'
            }
        }

        stage('Step 2') {
            when { 
                expression { fileExists('last_step.txt') && readFile('last_step.txt').trim() != 'Step 2' }
            }
            steps {
                echo 'Executing Step 2 print step2'
                writeFile file: 'last_step.txt', text: 'Step 2'
            }
        }

        stage('Step 3') {
            when { 
                expression { fileExists('last_step.txt') && readFile('last_step.txt').trim() != 'Step 3' }
            }
            steps {
                echo 'Executing Step 3'
                writeFile file: 'last_step.txt', text: 'Step 3'
            }
        }

        stage('Step 4') {
            when { 
                expression { fileExists('last_step.txt') && readFile('last_step.txt').trim() != 'Step 4' }
            }
            steps {
                echo 'Executing Step 4'
                writeFile file: 'last_step.txt', text: 'Step 4'
            }
        }
    }
}
