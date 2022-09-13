
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
   
                        sh(script: "${tool 'ansible 2.9'}/ansible all -i inventory.ini -m ping  --private-key=${keyfile} -u root")

                        }
                }
      }
      }
      }
     }
