
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
                    withCredentials([sshUserPrivatKey(credentialsId: 'Ansible2', KeyFileVariable: 'keyfile')]){
                        sh(script: "$(tool 'Ansible 2.9.23}/ansible all -i inventory -m ping --private-key=${keyfile} -u Ansible2")

                        }
                }
      }
      }
      }
     }
