pipeline {
    agent any
    stages {
        stage('Verificar a instalação do Docker' ){
            steps {
                echo 'Verificar a instalação do Docker'
                sh 'docker --version'
            }
            
        }
        stage('Construir imagem do frontend'){
            steps {
                echo 'Construir imagem do frontend - pablo/tarsbikecraft'
                dir('frontend'){
                     sh 'ls -la'
                     sh 'docker build -t pablo/tarsbikecraft .'
                     echo 'verificar se imagem foi criada'
                     sh 'docker images | grep pablo/tarsbikecraft || echo "Imagem não encontrada"'
                }
            }
        }
        stage('Subir Elasticsearch e Kibana'){
            steps{
                echo 'Executano docker-compose container Elasticsearch e Kibana'
                dir(..){
                    sh 'ls -la'
                    sh 'docker-compose up -d'
                    sh 'docker ps'
                    sh 'sleep 21'
                }
            }
        }

    }
}