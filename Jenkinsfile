#!groovy


pipeline {
    agent any
    
    parameters {
        
        choice(name: 'build_branch', choices: 'main' 'feature-branch', description: 'branches to be build', trim: true)
        choice(name: 'environments' choices: 'dev', description: 'select environments to be build')
        choice(name: 'version', choices: 'v.13', 'v.14', description: 'versions needs to release')
    }
    
   
      
    stages {
      stage('checkout') {
           steps {
             
                git  'https://github.com/devops4solutions/CI-example.git'
             
          }
        }
      }
      }
     
