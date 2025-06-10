pipeline {
    agent any
    
    stages {
        stage('Step 1') {
            steps {
                script {
                    def lastStep = fileExists('last_step.txt') ? readFile('last_step.txt').trim() : ""
                    if (lastStep != 'Step 1') {
                        echo 'Executing Step 1 print step1'
                        writeFile file: 'last_step.txt', text: 'Step 1'
                    } else {
                        echo 'Skipping Step 1'
                    }
                }
            }
        }
        
        stage('Step 2') {
            steps {
                script {
                    def lastStep = fileExists('last_step.txt') ? readFile('last_step.txt').trim() : ""
                    if (lastStep != 'Step 2') {
                        echo 'Executing Step 2 print step2'
                        writeFile file: 'last_step.txt', text: 'Step 2'
                    } else {
                        echo 'Skipping Step 2'
                    }
                }
            }
        }

        stage('Step 3') {
            steps {
                script {
                    def lastStep = fileExists('last_step.txt') ? readFile('last_step.txt').trim() : ""
                    if (lastStep != 'Step 3') {
                        echo 'Executing Step 3'
                        writeFile file: 'last_step.txt', text: 'Step 3'
                    } else {
                        echo 'Skipping Step 3'
                    }
                }
            }
        }

        stage('Step 4') {
            steps {
                script {
                    def lastStep = fileExists('last_step.txt') ? readFile('last_step.txt').trim() : ""
                    if (lastStep != 'Step 4') {
                        echo 'Executing Step 4'
                        writeFile file: 'last_step.txt', text: 'Step 4'
                    } else {
                        echo 'Skipping Step 4'
                    }
                }
            }
        }
    }
}
