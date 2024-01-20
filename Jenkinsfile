pipeline {
    agent any
    
    stages {
        stage("upload") {
            def inputFile = input message: 'Upload file', parameters: [file(name: 'data.zip')]
                new hudson.FilePath(new File("$workspace/data.zip")).copyFrom(inputFile)
                inputFile.delete()
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
