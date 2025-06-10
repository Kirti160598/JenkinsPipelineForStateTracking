def state = [:]
if (fileExists('./pipeline-state.json')) {
    state = readJSON file: './pipeline-state.json'
} else {
    state = [step1: "pending", step2: "pending", step3: "pending", step4: "pending"]
}
 
// STEP 1
if (state.step1 != "done") {
    stage('Step 1') {
        echo "Running Step 1"
        // do actual work...
        state.step1 = "done"
        writeJSON file: 'pipeline-state.json', json: state, pretty: 4
    }
}
 
// STEP 2
if (state.step2 != "done") {
    stage('Step 2') {
        echo "Running Step 2"
        // do actual work...
        state.step2 = "done"
        writeJSON file: 'pipeline-state.json', json: state, pretty: 4
    }
}
 
// STEP 3
if (state.step3 != "done") {
    stage('Step 3') {
        echo "Running Step 3"
        // do actual work...
        state.step3 = "done"
        writeJSON file: 'pipeline-state.json', json: state, pretty: 4
    }
}
 
// STEP 4
if (state.step4 != "done") {
    stage('Step 4') {
        echo "Running Step 4"
        // do actual work...
        state.step4 = "done"
        writeJSON file: 'pipeline-state.json', json: state, pretty: 4
    }
}
