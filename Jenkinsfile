pipeline {
    agent any

    stages {

        stage("backup") {
            when { expression { return !fileExists ('/etc/hosts.jenkins.bak') } }
            steps {
                script {
                    echo "'/etc/hosts.bak' Not found, do a backup now"
                    sh "cp /etc/hosts /etc/hosts.jenkins.bak"
                }
            }
        }
    }
}

