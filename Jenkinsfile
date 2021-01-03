node{

    stage('SCM Checkout')
    {
        git credentialsId: 'ba8f2503-3401-41c4-93e4-cd5a0f4ba9c6', url: 'https://github.com/Raksniru/online-shop.git'
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
             sh 'docker push nameisnani/job1_web2.0:635fd28d7af5'
            // sh 'docker push nameisnani/mysql'
          
    }
}
