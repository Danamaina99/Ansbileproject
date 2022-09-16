#!groovy


pipeline {
    agent any
    
    parameters {
        
        booleanParam(name: "TEST_BOOLEAN", defaultValue: true, description: "Sample boolean parameter")
        string(name: "TEST_STRING", defaultValue: "ssbostan", trim: true, description: "Sample string parameter")
        text(name: "TEST_TEXT", defaultValue: "Jenkins Pipeline Tutorial", description: "Sample multi-line text parameter")
        password(name: "TEST_PASSWORD", defaultValue: "SECRET", description: "Sample password parameter")
        //choice(name: "TEST_CHOICE", choices: ["production", "staging", "development"], description: "Sample multi-choice parameter")
        //choice(name: 'build_branch', choices: 'main' 'feature-branch', description: 'branches to be build', trim: true)
        choice(name: "ENVIRONMENTS", choices: ["dev", "uat"], description: "select environments to be build")
        //choice(name: 'version', choices: 'v.13', 'v.14', description: 'versions needs to release') 
    }
    
   
      
    stages {
      stage('checkout') {
           steps {
             
                git  'https://github.com/devops4solutions/CI-example.git'
             
          }
        }
      }
      }
     
