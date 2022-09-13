
pipeline {
    agent any
    tools {
      ansible 'Ansible 2.9.23'
    } 
     
    stages {
      stage('checkout') {
           steps {
             
                git  'https://github.com/devops4solutions/CI-example.git'
             
          }
        }
        
 
        
     stage('Ansible Deploy') {
             
            steps {
                script {
                    withCredentials([sshUserPrivateKey(credentialsId: 'ansible', keyFileVariable: 'keyfile')]) {
   
                        sh(script: "${tool 'Ansible 2.9.23'}/ansible-playbook all -i inventory.ini -m ping --private-key=${keyfile} -u root")

                        }
                }
      }
      }
      }
     }
