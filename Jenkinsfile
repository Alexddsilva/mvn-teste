pipeline {
    agent any

    environment {
        PATH = "/usr/local/bin:$PATH"
    }
    
    stages {
        stage('test mvn') {
            steps {
                script {
                    docker.image('maven:3.8-eclipse-temurin-11-focal').inside {
                        println('starting docker process')
                        git 'https://bitbucket.org/avioconsulting/mvn-test/src/master/'
                    }
                    
                }
            }
        }
    }
}
