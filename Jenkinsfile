pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }
        stage('Convert & Train') {
            steps {
                // jupyter 명령어가 배스(bash)에서 실행되도록 설정
                sh "jupyter nbconvert --to script main.ipynb"
                // 변환된 파이썬 스크립트 실행 (python3 명령어 사용)
                sh "python3 main.py"
            }
        }
    }
}
