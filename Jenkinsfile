pipeline {
    agent none
    stages {
        stage('Build') {
            agent any
            steps {
                sh 'pyinstaller add2vals.py -F'
                stash(name: 'compiled-results', includes: 'sources/*.py*')
            }
        }
    }
}
