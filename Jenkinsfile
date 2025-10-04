pipeline { 
  
  agent { 
    label {
      label "Slave-1"
      customWorkspace "/mnt/mainBranch" 
    } 
  
  }
  stages { 
    stage ("one") { 
      steps { 
        echo "This is main branch" 
      } 
    } 
  } 
}
