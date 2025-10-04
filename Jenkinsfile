pipeline { 
  
  agent { 
    label {
      label "Slave-1"
      customWorkspace "/mnt/slave-1" 
    } 
  
  }
  stages { 
    stage ("one") { 
      steps { 
        echo "This is master branch" 
      } 
    } 
  } 
}
