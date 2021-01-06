node{

    stage('SCM Checkout')
    {
        git credentialsId: '084a0c30-7b5f-45df-b39b-a390983bbb33', url: 'https://github.com/Raksniru/online-shop.git'
    }
    
    stage('Run Docker Compose File')
    {
        
        sh 'docker-compose build'
        sh 'docker-compose up -d'
    }
  stage('PUSH image to Docker Hub')
    {
      /* withCredentials([string(credentialsId: 'DockerHubPassword', variable: 'DHPWD')]) 
        {
            sh "docker login -u nameisnani -p ${DHPWD}"
        }
        sh 'docker push vardhanns/phpmysql_app'
        */
        //docker.withRegistry( 'https://registry.hub.docker.com', 'DockerHubPassword' ) {
             
             sh 'docker login -u "nameisnani" -p "Madman@64" docker.io'
             //sh 'docker push nameisnani/mysql'
             //sh 'docker push nameisnani/job1_web1.0'
             sh 'docker push nameisnani/job1_web2.0:latest'
            // sh 'docker push nameisnani/mysql'
          
    }
}
