pipeline { 
  agent { 
    label { 
      label "Slave-1" 
      customWorkspace "/mnt/21q1Branch" 
    } 
  } 
  stages{ 
    stage ("one")  { 
      steps { 
        echo "This is 21q1 branch"
      }
    } 
  } 
  stage("two"){
    steps{
        sh "docker run -dp 80:80 --name c2 httpd"
        sh "dcker cp /mnt/21q1Branch/index.html c2:/usr/local/apache2/htdocs"
        sh "docker exec chmod -R 777 /usr/local/apache2/htdocs"
    }

  }
}
