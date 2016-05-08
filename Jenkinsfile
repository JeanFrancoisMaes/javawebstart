node {
   
    stage 'cleaning workspace'
 sh'rm -rf *'
   // Mark the code checkout 'stage'....
   stage 'Checkout'

   // Get some code from a GitHub repository
   git url: 'https://github.com/JeanFrancoisMaes/javawebstart'

   
   stage 'Build'
    docker.build('javawebstart:latest')
    
    stage 'Run docker container'
    docker.image('javawebstart').run('-d-p 80:80')
 

 
}
