
pipeline {
    agent any
    
    parameters {
        
        string(defaultValue: 'V.13', description: 'Release version. eg 1.0.0', name: 'RELEASE_VERSION', trim: true)
        choice(name: 'ENVIRONMENT', choices: environments, description: 'Environment')
               }
        
        
   
    stages {
      stage('checkout') {
           steps {
             
                git  'https://github.com/devops4solutions/CI-example.git'
             
          }
        }
      }
      }
     
