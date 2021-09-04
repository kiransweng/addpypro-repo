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

  }
}