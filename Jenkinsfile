pipeline {
    agent none
    stages {
        stage('Build') {
            agent any
            steps {
                sh 'python3 -O -m PyInstaller -F sources/add2vals.py'
                stash(name: 'compiled-results', includes: 'sources/*.py*')
            }
        }
    }
}
