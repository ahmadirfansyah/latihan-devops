pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Mengambil kode dari GitHub...'
                git 'https://github.com/username/latihan-devops.git'
            }
        }
        stage('Build Docker Image') {
            steps {
                echo 'Sedang membungkus aplikasi ke Docker...'
                sh 'docker build -t aplikasi-devops .'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Menjalankan aplikasi di server...'
                sh 'docker run -d --name kontainer-app aplikasi-devops'
            }
        }
    }
}





