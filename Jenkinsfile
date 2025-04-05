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
                sh 'ls -la'
              
            }
        }
    }
}