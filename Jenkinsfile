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
               
                        ansiblePlaybook(
             credentialsId: 'Ansible2', 
             disableHostKeyChecking: true, 
             installation: 'ansible2', 
             inventory: 'inventory.ini', 
             playbook: 'apache.yml'
         )

}
}
}
    }
}

