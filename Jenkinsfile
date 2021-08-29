pipeline {
  agent {
    node {
      label 'kiransys'
    }

  }
  stages {
    stage('add') {
      steps {
        dir(path: 'cd addpro/src/org/programs') {
          bat(script: 'python Addition.py', label: 'kiransys')
        }

      }
    }

    stage('sub') {
      steps {
        git(url: 'https://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@github.com/kiransweng/subpypro-repo.git', branch: 'main')
        bat(script: 'cd subpro\\src\\org\\programs', label: 'kiransys')
        bat(script: 'python Substract.py', label: 'kiransys')
      }
    }

    stage('multi') {
      steps {
        git(url: 'https://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@github.com/kiransweng/multipypro-repo.git', branch: 'main')
        bat(script: 'cd multipro\\src\\org\\programs', label: 'kiransys')
        bat(script: 'python Multiply.py', label: 'kiransys')
      }
    }

  }
}