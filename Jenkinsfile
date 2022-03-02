node {
 def app
   stage ('Clone') {
        checkout scm
     } 
   stage ('Build image') {
     app= docker.build ("Alpine")
   } 

   stage ('Run image') {
      docker.image('Alpine').withRun('-p 80:80') {   c->
      sh 'docker build'
     sh 'curl localhost'
    } 
  }
}
