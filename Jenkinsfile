pipeline {
    agent { label 'node' }
    triggers { pollSCM('* * * * * 1') }
        stages {
            stage('vcs') {
                steps {
                    git url: 'git@github.com:tejachennuru1/ansible31123.git'
                    branch: 'main'
                }
            }
        }
        stage {
            steps {
                sh 'ansible-playbook -i hosts openjdk.yaml'
                sh 'ansible-playbook -i hosts ansible.yaml'
            }
        }

}
