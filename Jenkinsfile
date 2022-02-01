pipeline {
    agent any

    stages {
        stage('Get_Code_ blaster') {
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
                sh 'scp target/sparkjava-hello-world-1.0.war root@172.17.0.4:/var/lib/apache-tomcat-9.0.56/webapps'
            }
        }
    }
}
