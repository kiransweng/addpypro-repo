pipeline {
  agent {
    node {
      label 'kiransys'
    }

  }
  stages {
    stage('add') {
      steps {
        dir(path: 'addpro\\src\\org\\programs') {
          bat(script: 'python Addition.py', label: 'kiransys')
        }

      }
    }

    stage('sub') {
      steps {
        git(url: 'https://github.com/kiransweng/subpypro-repo.git', branch: 'main', credentialsId: 'kiransweng')
        dir(path: 'subpro\\src\\org\\programs')
        bat(script: 'python Substract.py', label: 'kiransys')
      }
    }

  }
}