pipeline {
    agent any

    stages {
        stage('Checkout SCM') {
            steps {
                // GitHub에서 코드 받아오기 (Jenkins 설정에서 이미 정의돼 있음 → 생략 가능)
                echo 'SCM Checkout 자동 수행됨'
            }
        }

        stage('Compile') {
            steps {
                echo '컴파일 단계 실행'
                sh './gradlew compileJava'
            }
        }

        stage('Build') {
            steps {
                echo '빌드 단계 실행'
                sh './gradlew build'
            }
        }

        stage('Unit test') {
            steps {
                echo '테스트 단계 실행'
                sh './gradlew test'
            }
        }
    }
}
