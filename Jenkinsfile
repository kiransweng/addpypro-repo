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
        git(url: 'https://github.com/kiransweng/subpypro-repo.git', branch: 'main', credentialsId: 'af366798-2ee9-4a5b-a0bc-57d11783f417')
        dir(path: 'subpro\\src\\org\\programs') {
          bat(script: 'python Substract.py', label: 'kiransys')
        }

      }
    }

    stage('multi') {
      steps {
        git(url: 'https://github.com/kiransweng/multipypro-repo.git', branch: 'main', credentialsId: 'af366798-2ee9-4a5b-a0bc-57d11783f417')
        dir(path: 'multipro\\src\\org\\programs') {
          bat(script: 'python Multiply.py', label: 'kiransys')
        }

      }
    }

  }
}