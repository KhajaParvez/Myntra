pipeline {
    agent none

    parameters {
        // booleanParam, choice, file, text, password, run, or string
        booleanParam(defaultValue: true, description: '', name: 'booleanExample')
        string(defaultValue: "Kp", description: 'What environment?', name: 'stringExample')
        text(defaultValue: "This is a multiline\n text", description: "Multiline Text", name: "textExample")
        choice(choices: 'US-EAST-1\nUS-WEST-2', description: 'What AWS region?', name: 'choiceExample')
        password(defaultValue: "Password", description: "Enter your password", name: "passwordExample")
    } 

    stages {
        stage("Build") {
            steps {
                echo "booleanExample: ${params.booleanExample}"
				}
			}
		stage("Build 2") {
			steps {
                echo "stringExample: ${params.stringExample}"
                echo "textExample: ${params.textExample}"
				}
			}
		stage("Final Build") {
			steps {
                echo "choiceExample: ${params.choiceExample}"
                echo "passwordExample: ${params.passwordExample}"
				}
            }
        }
    }