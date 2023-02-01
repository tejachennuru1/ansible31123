pipeline {
    agent{label "ansible"}
    triggers { pollSCM('* * * * *') }
    stages {
        stage('vcs') {
            steps {
                git branch:'main',url:'https://github.com/tejachennuru1/ansible31123.git'
            }
        }
        stage('ansible') {
            steps {
                sh 'ansible-playbook -i hosts ansible.yaml'
            }
        }
    }
}
