pipeline { 
  agent { 
    label { 
      label "Slave-1" 
      customWorkspace "/mnt/mainBranch" 
    } 
  } 
  stages{ 
    stage ("one")  { 
      steps { 
        echo "This is main branch"
      }
    } 
  } 
  stage("two"){
    steps{
        sh "docker run -dp 90:80 --name c1 httpd"
        sh "dcker cp /mnt/mainBranch/index.html c1:/usr/local/apache2/htdocs"
        sh "docker exec c1 chmod -R 777 /usr/local/apache2/htdocs"
    }

  }
}
