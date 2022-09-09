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
                 
           ansiblePlaybook credentialsId: 'Ansible2', disableHostKeyChecking: true, installation: 'ansible2', inventory: 'Ansibleproject/inventory.ini', playbook: 'Ansibleproject/apache.yml'
} 
}
}
}
