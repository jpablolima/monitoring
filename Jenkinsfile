pipeline {
    agent any
    stages {
        stage('Verificar a instalação do Docker' ){
            steps {
                echo 'Verificar a instalação do Docker'
                sh 'docker --version'
            }
            
        }
        stage("Criação do diretório do Elasticsearch ") {
            steps{
                echo 'Criação e configuração do diretório do Elasticsearch '
                sh 'sudo chown -R 1000:1000 /opt/elasticsearch/data'
                sh 'sudo chmod -R 775 /opt/elasticsearch/data'
            }

        }
        stage('Construir imagem de monitoramento - Elasticsearch e Kibana'){
            steps {
                echo 'Construir imagem de monitoramento - Elasticsearch e Kibana'

                    echo "vericiar arquivos"
                    sh 'ls -la'
                    echo "Construir imagen do Elasticsearch e Kibana"
                    sh "docker-compose up -d"
                
            }
        }
     }
}      
                
            
