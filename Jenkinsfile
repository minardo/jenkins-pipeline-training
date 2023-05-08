pipeline {
    agent {
        node {
            label "linux && java11"
        }
    }
    stages {
        stage("Build") {
            steps {
                script {
                    for (int i=0; i<10; i++) {
                        echo("Script ${i}")
                    }
                }
                echo("Start Build")
                sh("./mvnw clean compile test-compile")
                echo("Finish Build")
            }
        }
        stage("Test") {
            steps {
                echo("Start Test")
                sh("./mvnw test")
                echo("Finish Test")
            }
        }
        stage("Deploy") {
            steps {
                echo "Hello Deploy 1"
                sleep(5)
                echo "Hello Deploy 2"
                echo "Hello Deploy 3"
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