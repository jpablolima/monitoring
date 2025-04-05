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
        stage('Executar container para  verificação de teste...'){
            steps{
                echo 'Executar container...'
                sh 'docker run --name tartarsbikecraft -p 8181:80 pablo/tarsbikecraft -d'
                sh 'docker ps'
            }
        }

    }
}