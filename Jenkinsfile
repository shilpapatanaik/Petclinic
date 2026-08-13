node {
    stage('Clone') {
        git branch: 'main', url: 'git@github.com:shilpapatanaik/Petclinic.git'
    }
     stage('Build') {
        bat 'mvn clean install'
    }
      stage('Test the war') {
                echo ("deploy contextPath: null, war: 'target/*.jar''")
                
    }    
      stage('artifacts') {
        archiveArtifacts artifacts: 'target/*.jar', followSymlinks: false
                
    }
      stage('Generate Test Report') {
         junit 'target/surefire-reports/*.xml'
    }
      stage('Deploy'){
           echo 'Deploy the project'
    }

}