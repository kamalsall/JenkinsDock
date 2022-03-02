node {
 def app
   stage ('Clone') {
        checkout scm
     } 
   stage ('Build image') {
     app= docker.build ("alpine")
   } 

   stage ('Run image') {
      docker.image('alpine').withRun('-p 80:80') {   c->
      sh 'docker ls'
     
    } 
  }
}
