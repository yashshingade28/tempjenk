pipeline {
    agent any
    
    stages {
        stage('User Input') {
            steps {
                script {
                    // Use the input step to prompt the user for a file
                    def userInput = input(
                        id: 'fileInput',
                        message: 'Please upload a file',
                        parameters: [file(name: 'FILE')]
                    )
                    
                    // Access the selected file
                    def selectedFile = userInput['FILE']
                    
                    // Now you can use 'selectedFile' in your build steps
                    echo "Selected file: ${selectedFile}"
                }
            }
        }
        
        stage('Install Dependencies') {
            steps {
                echo "first step"
            }
        }

        stage('Build') {
            steps {
                echo "second step"
            }
        }
    }
}
