pipeline {
    agent any

    environment {
        GIT_REPO = 'https://github.com/MayankSaxena23/AI-Image-Generator.git'
        BRANCH = 'main'
    }

    stages {
        stage('Checkout Code') {
            steps {
                git branch: "${BRANCH}", url: "${GIT_REPO}"
            }
        }

        stage('Show Git Changes') {
            steps {
                script {
                    echo "Recent Git Commits:"
                    sh 'git log -3 --oneline'
                    
                    echo "Changed Files in Last Commit:"
                    sh 'git diff --name-only HEAD~1 HEAD'
                }
            }
        }
    }
}
