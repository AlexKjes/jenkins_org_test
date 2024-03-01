pipeline {

    agent any

    stages{
        stage("Hello World") {
            steps {
                echo "This pipeline works! Or at least this stage"
            }
        }

        stage("Docker") {
            stage{
                docker.withRegistry("http://registry-docker-registry:8080") {
                    def testImage docker.pull("hello-world:linux")
                    echo "Pulled docker image successfully"
                }
            }
        }
    }
}
