pipeline {
 agent { 
    node { label 'maven' }      
 }  
 environement {
   def constants = load 'constants.groovy'
  def giturl = constants.giturl
 }
stages {
 
stage('git clone') {   
steps {
 
 //script {
  //def constants = load 'constants.groovy'
 // def giturl = constants.giturl
  //sh "echo ${giturl}"
  git url: "${giturl}"
 //}
  //git url: "${giturl}"
 //git url: 'https://github.com/shweta9651/java-junit-sample.git'
// git url: 'https://github.com/miguno/java-docker-build-tutorial.git'  

}
}  

stage('compile source code') {
     steps {
         sh 'mvn clean install'
   
     }
  }
    
 }
}   
 
