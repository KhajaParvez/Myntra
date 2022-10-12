pipeline {
    agent any

    parameters {
        // booleanParam, choice, file, text, password, run, or string
        booleanParam(defaultValue: false, description: '', name: 'booleanExample')
        string(defaultValue: "INDIA", description: 'What environment?', name: 'stringExample')
        text(defaultValue: "This is a DevOps project\n text", description: "Multiline Text", name: "textExample")
        choice(choices: 'US-WEST-2\nUS-EAST-1', description: 'What AWS region?', name: 'choiceExample')
        password(defaultValue: "Password", description: "Enter your password", name: "passwordExample")
    } 

    stages {
        stage("Test case1") {
            steps {
                echo "booleanExample: ${params.booleanExample}"
				}
			}
		stage("Data") {
			steps {
                echo "stringExample: ${params.stringExample}"
                echo "textExample: ${params.textExample}"
				}
			}
		stage("Final Stage") {
			steps {
                echo "choiceExample: ${params.choiceExample}"
                echo "passwordExample: ${params.passwordExample}"
				}
            }
        }
   }
