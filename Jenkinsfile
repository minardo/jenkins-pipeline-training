pipeline {
    agent {
        node {
            label "linux && java11"
        }
    }
    stages {
        stage("Build") {
            steps {
                echo "Hello Pipeline"
            }
        }
        stage("Test") {
            steps {
                echo "Hello Pipeline"
                sh("error")
            }
        }
        stage("Deploy") {
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