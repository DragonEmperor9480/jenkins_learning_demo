pipeline{
    agent any
    stages{
        stage('clone Repositry'){
            steps{
                git branch: 'main', url: 'https://github.com/DragonEmperor9480/jenkins_learning_demo.git'
            }
        }
        stage('Build'){
            steps{
                echo "Building web app"
            }
        }
        stage('Deploy'){
            steps{
                echo "Deploying web app"
                sh 'cp -r * /var/www/html/'
            }
        }
    }
}