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

                     sh 'ls -la'
                    //  sh 'docker build -t pablo/tarsbikecraft .'
                    //  echo 'verificar se imagem foi criada'
                    //  sh 'docker images | grep pablo/tarsbikecraft || echo "Imagem não encontrada"'
                
            }
        }
       
                
                    
              
}


