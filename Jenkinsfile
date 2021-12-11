pipeline{
  agent any
  tool { maven3.8 'maven' }
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
    
