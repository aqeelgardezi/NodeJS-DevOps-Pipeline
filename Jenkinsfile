pipeline {
  agent any

  stages {
    stage('Checkout SCM') {
      steps {
        // Checkout source code from GitHub
        git branch: 'main', url: 'https://github.com/aqeelgardezi/NodeJS-DevOps-Pipeline.git'
      }
    }

    stage('OWASP Dependency Check') {
      steps {
        script {
          dependencyCheck additionalArguments: '', 
                          odcInstallation: 'Dependency-Check', 
                          scanpath: '.', 
                          outdir: 'dependency-check-report'
        }
      }
    }
  }
}
