pipeline {
    agent {
        node {
            label "linux && java11"
        }
    }
    stages {
        stage("Hello") {
            steps {
                echo "Hello Pipeline"
            }
        }
    }
    post {
        always {
            echo "akan selalu tampil tidak peduli statusnya apa"
        }
        success {
            echo "akan tampil jika statusnya berhasil"
        }
        failure {
            echo "akan tampil jika statusnya gagal"
        }
        cleanup {
            echo "tidak peduli statusnya berhasil atau error"
        }
    }
}