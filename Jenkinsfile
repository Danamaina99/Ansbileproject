
pipeline {
    agent any
    
    
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
   
                        sh(script: "ansible-playbook all -i inventory.ini -vvv apache.yml -m ping --private-key=${keyfile} -u root")

                        }
                }
      }
      }
      }
     }
