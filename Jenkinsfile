pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh '''
                    echo "Building Java project..."
                    cd "Password Protection"
                    mkdir -p build
                    javac -d build src/*.java
                '''
            }
        }
        stage('Deploy') {
            steps {
                sh '''
                    cd "Password Protection"
                    jar cf FileEncrypter.jar -C build .
                '''
            }
        }
    }
}
