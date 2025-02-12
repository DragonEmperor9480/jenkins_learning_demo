pipeline {
    agent any

    triggers {
        githubPush()  // This tells Jenkins to trigger when GitHub sends a webhook
    }

    stages {
        stage('Clone Repository') {
            steps {
                git 'https://github.com/DragonEmperor9480/jenkins_learning_demo.git'
            }
        }
        stage('Build') {
            steps {
                echo 'Building web app'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying web app'
                sh 'sudo cp -r index.html Jenkinsfile script.js styles.css /var/www/html/'
            }
        }
    }
}
