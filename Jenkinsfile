pipeline {

    agent any

    stages {
        stage('mysql') {
            agent {
                docker {
                    image 'kharchenkov/mysql'
                    args '-e MYSQL_ROOT_PASSWORD=pass -v db:/var/lib/mysql '
                }
            }
        }
        stage('php'){
            agent{
                docker{
                    image 'kharchenkov/php'
                    args '-p 80:80 -v ./html:/var/www/html'
                }
            }
        }


    post {
        always {
            echo "Job is finished"
        }
        success {
            echo "success"
        }
        failure {
            echo "failure"
        }
        aborted {
            echo "aborted"
        }
    }
}