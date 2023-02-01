pipeline {
    agent { label: "node" }
     triggers { pollSCM('* * * * *') }
      stages {
        stage(vcs) {
            steps {
                git branch:"main",url: "https://github.com/ramesh1469/ansibletask.git"
             }
        }
       stage(ansible) {
          steps {
            sh "ansible-playbook -i hosts ansible.yaml"
          }
       }
   }
}