pipeline {
    agent any
    stages {
        stage('Clone Repo') {
            steps {
                git branch: 'master',
                    url: 'https://github.com/tashin954/time-tracker.git'
            }
        }
    }
}
