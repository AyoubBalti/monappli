pipeline{
  agent any
  tool name: 'maven3.8', type: 'maven'
  stages{
    stage ("Delete workspace") {
      steps {
        cleanWs deleteDirs:true
        checkout scm
      }
    }
    stage ("Build monappli"){
      steps{
        bat """ mvn clean install """ }
    }
  }
}
    
