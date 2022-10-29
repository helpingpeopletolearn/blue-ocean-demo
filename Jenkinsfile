pipeline {
  agent any
  stages {
    stage('Fetch Code') {
      steps {
        git(url: 'git@github.com:helpingpeopletolearn/blue-ocean-demo.git', branch: 'main')
      }
    }

    stage('Install Apache') {
      steps {
        sh 'sudo apt install apache2 -y'
      }
    }

    stage('Deploy Application') {
      steps {
        sh 'sudo cp -R * /var/www/html/'
      }
    }

  }
}