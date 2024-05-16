pipeline {
    agent any
    environment {
        ANSIBLE_HOME = tool name: 'ansible', type: 'hudson.plugins.ansible.AnsibleInstallation'
    }
    stages{
        stage("ExecutePlaybook"){
            steps{
               ansiblePlaybook become: true, credentialsId: 'AnsibleUser_sanjay', disableHostKeyChecking: true, installation: "${ANSIBLE_HOME}", inventory: '/Ansible/inventory', playbook: '/Ansible/install_git.yml', vaultTmpPath: '' 
            }
        }
    }
}
