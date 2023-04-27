pipeline {
    agent any

    stages {
        stage('Playbook') {
            steps {
                script {
                    withEnv(["PATH+ANSIBLE=${tool 'ansible_lemp'}"]) {
                        ansiblePlaybook(
                            playbook: 'lemp_playbook.yml',
                            inventory: 'inventory.ini',
                            disableHostKeyChecking: true
                        )
                    }
                }
            }
        }
    }
}
