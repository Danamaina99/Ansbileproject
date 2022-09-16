#!groovy


pipeline {
    agent any
    
    parameters {
        
        choice(name: 'version', choices: 'v.13, v.14', description: 'versions needs to release')
    }
    
   
      
    stages {
      stage('checkout') {
           steps {
             
                git  'https://github.com/devops4solutions/CI-example.git'
             
          }
        }
      }
      }
     
