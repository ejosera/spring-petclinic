pipeline {
    agent { docker 'maven:3.6.1-alpine' }
    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/ejosera/spring-petclinic.git'
            }
        }
        stage ('Build'){
            steps {
                sh 'mvn clean package'
		junit '**/target/surefire-reports/TEST-*.xml'
            }
        }
    }
}
