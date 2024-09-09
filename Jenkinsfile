pipeline {
    agent any

   

    stages {
        stage('Trigger CodeBuild') {
            steps {
                sh 'aws codebuild start-build --project-name PracticeAWS --source-version main --region ap-south-1'
            }
        }
    }

}

