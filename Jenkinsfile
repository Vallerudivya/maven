pipeline {
    agent any

    stages {
        stage('Get_Code_Master') {
            steps {
                git 'https://github.com/AneesRavidKhan/DemoATC.git'
            }
        }
        stage('Build_Code') {
            steps {
                sh 'mvn install'
            }
        }
        stage('Deploy') {
            steps {
                sh 'sshpass -p "suri" scp target/DemoATR.war root@172.17.0.3/var/lib/tomcat9/webapps'
            }
        }
    }
}
