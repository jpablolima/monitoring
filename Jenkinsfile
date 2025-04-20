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
                sh 'sudo cp -R --exclude=".git" . /var/www/html'

                // sh 'cp -R . /var/www/html'
            }
        }
        stage('Restart do Nginx') {
            steps {
                sh 'sudo systemctl restart nginx'
                sh 'sudo systemctl status nginx'
            }
        }
    }
}