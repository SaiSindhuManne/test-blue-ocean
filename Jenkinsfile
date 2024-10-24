pipeline {
  agent any
  stages {
    stage('Fetch Code') {
      steps {
        git(url: 'https://github.com/SaiSindhuManne/test-blue-ocean.git', branch: 'main')
      }
    }

    stage('Install apache') {
      steps {
        sh 'sudo apt install apache2 -y'
      }
    }

    stage('Deploy App') {
      steps {
        sh 'sudo cp -R * /var/www/html/'
      }
    }

  }
}