node {
 def app
   stage ('Clone') {
        checkout scm
     } 
   stage ('Build image') {
     app= docker.build ("alpine")
   } 

   stage ('Run image') {
      docker.image('alpine'){   c->
      sh 'docker ls'
     
    } 
  }
}
