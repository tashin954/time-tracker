pipeline {
    agent any
    stages {
        stage('Clone Repo') {
            steps {
                git branch: 'master',
                    url: 'https://github.com/tashin954/time-tracker.git'
            }
        }
                stage('zip file') {
            steps {
                sh 'zip -r $GIT_COMMIT.zip /var/lib/jenkins/workspace/"Clone GitHub Repo"'
            }
        }

                stage('upload to s3') {
            steps {
                sh 'aws s3 cp $GIT_COMMIT.zip s3://git-hub-clone/'
            }
        }
    }
}
