pipeline{
    agent any
    stages{
        stage('SCM Checkout'){        
            steps{
            git 'https://github.com/Pavanlee007/myapp-ansible'
        }
    }
    stage('Excecute Ansible'){
        steps{
             ansiblePlaybook credentialsId: 'private-key', installation:'ansible2', inventory: 'dev.inv', playbook: 'apache.yml'
        }
    }
  }
}
