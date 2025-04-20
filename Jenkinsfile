pipeline {
    agent any
    stages {
        stage('Deploy do Front-end' ){
            steps {
                echo 'Verificar se o Nginx está instalado....'
                sh 'nginx -v'
            }
            
        }
        stage('Deploy do Front-End'){
            steps {
                echo 'Vefiricando diretório'
                sh 'ls -la'
                sh 'cp -R . /var/www/html'
            }
        }
    }
}