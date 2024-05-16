pipeline {
    agent any
    stages{
        stage("ExecutePlaybook"){
            steps{
               ansiblePlaybook become: true, credentialsId: 'AnsibleUser_sanjay', disableHostKeyChecking: true, installation: 'AnsibleBuilds', inventory: '/Ansible/inventory', playbook: '/Ansible/install_git.yml', vaultTmpPath: '' 
            }
        }
    }
}
