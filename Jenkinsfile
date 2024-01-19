pipeline {
    agent any

    stages {

        stage("backup") {
            when { expression { return !fileExists ('/etc/hosts.jenkins.bak') } }
            steps {
                script {
                    echo "'/etc/hosts.jenkins.bak' Not found, do a backup first"
                    sh "cp /etc/hosts /etc/hosts.jenkins.bak"
                }
            }
        }

        stage("update") {
            steps {
                script {
                    echo "Download github hosts"
                    sh "curl -o /etc/hosts.hellogithub https://raw.hellogithub.com/hosts"

                    echo "Empty source hosts"
                    sh "> /etc/hosts"

                    echo "Merge hosts"
                    sh "cat /etc/hosts.jenkins.bak /etc/hosts.hellogithub > /etc/hosts"
                }
            }
        }
        
    }
}

