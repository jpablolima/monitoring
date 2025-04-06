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
                echo 'Construir imagem de monitoramento - Elasticsearch e Kibana'

                    echo "vericiar arquivos"
                    sh 'ls -la'
                    echo "Construir imagen do Elasticsearch e Kibana"
                    sh "docker-compose up -d"
                
            }
        }
       
                
            
    }
}