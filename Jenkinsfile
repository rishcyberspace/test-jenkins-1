

pipeline {
    agent { label 'master' }
    options([parameters([booleanParam(defaultValue: true, description: 'hello', name: 'gagan'), choice(choices: ['aaa , b ,  c '], description: 'd', name: 'choice'), run(description: 'df', filter: 'ALL', name: 'dfds', projectName: 'fds')])])
    stages {
        stage('pre build') {
            steps {
                // Clean before build
                cleanWs()
                // We need to explicitly checkout from SCM here
                checkout scm
                echo "Building ${env.JOB_NAME}..."
            }

        }

        stage('cloning second repo ') {
            steps {
                echo 'Make the output directory'
                sh 'mkdir -p testdir'
                dir('testdir') {
                git branch: 'main', credentialsId: '91f5e3a6-48b2-4204-a476-96b771afaef3', url: 'https://github.com/gagan4491/test-jenkins.git'
            }
            }
         }

        stage('build') {
            steps {
                echo "Hello World!guys"
                sh 'printenv'
                sh 'pwd'
                echo "done "
                echo 'Make the output directory'
                sh 'mkdir -p testdir'
                dir('testdir') {
                git branch: 'main', credentialsId: '91f5e3a6-48b2-4204-a476-96b771afaef3', url: 'https://github.com/gagan4491/test-jenkins.git'
      }
        }
    }
}
}
