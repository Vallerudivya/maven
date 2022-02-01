pipeline {
    agent any

    stages {
        stage('Get_Code_Master') {
            steps {
                git 'https://github.com/boxfuse/boxfuse-sample-java-war-hello.git'
            }
        }
        stage('Build_Code') {
            steps {
                sh 'mvn install'
            }
        }
        stage('Deploy') {
            steps {
                sh 'sshpass -p "suri" scp target/sparkjava-hello-world-1.0.war root@172.17.0.3/var/lib/apache-tomcat-9.0.56/webapps'
            }
        }
    }
}
