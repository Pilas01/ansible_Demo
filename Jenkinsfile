pipeline{
  agent any  
  stages{  
      stage("Run an ansible playbook"){
        steps{
          ansiblePlaybook credentialsId: 'SSH-KEY', inventory: 'hosts', playbook: 'nginx_install.yaml'
        }
      }
      stage("Print Nginx Installed"){
        steps{
           sh"echo nginx installed on all servers"
        }
      }
  }
}
