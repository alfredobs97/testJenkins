pipeline {
// definimos que nodo va a ejecutarlo
  agent any

  //plugins que va a usar
  tools {nodejs "node"}
    
  stages {
        
    stage('Cloning Git') {
      steps {
        git ( 
            url:'https://github.com/alfredobs97/testJenkins',
            credentialsId: '4a47ed5b-8571-4c55-b4bc-e8aad7010568	'
            )
        
      }
    }
        
    stage('Install dependencies') {
      steps {
        sh 'npm install'
      }
    }
    
    stage('Test') {
      steps {
         sh 'npm test'
      }
    }      
  }
}