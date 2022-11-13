pipeline {
    agent any
    stages {
        stage('Example') {
            input {
                message "Should we continue?"
                ok "Yes, we should."
                submitter "alice,bob"
                parameters {
                    string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I greet?')
                }
            }
            when {
                equals expected: "Fred", actual: "${PERSON}"
            }
            steps {
                echo "Hello, ${PERSON}, nice to meet you."
            }
        }
    }
}
