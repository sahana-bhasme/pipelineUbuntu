
pipeline {
    agent any
    triggers {
        cron('H/10 * * * *')
    }
    stages {
        
        stage("compile") {
            steps {
                sh 'mvn  compile'
            }
        }
        
        stage("Testing") {
            steps {
                sh 'mvn test'
            }
        }

        stage("Build") {
            steps {
                sh 'mvn package'
            }
        }
    }
}
