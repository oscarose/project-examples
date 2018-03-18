node {
   def commit_id
   stage('Readiness') {
     checkout scm
     sh "git rev-parse --short HEAD > .git/commit-id"                        
     commit_id = readFile('.git/commit-id').trim()
   }
    stages {
        stage('build') {
            steps {
                sh 'mvn --version'
            }
        }
    }
}

