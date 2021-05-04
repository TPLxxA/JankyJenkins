// Quick start declarative pipeline for Python
pipeline {
    agent {
        docker {
            image 'python:3.5.1'
            }
        }
    environment {
        ENV_VAR = 'globaal'
        GLB_INT = 12
    }
    stages {
        stage('build') {
            steps {
                sh 'python --version'
                echo "NV_VAR is ${ENV_VAR}"
                echo "${GLB_INT} is an integer"
                sh 'printenv'
            }
        }
    }
    post {
        succes {
            mail to: 'casper@techgrounds.nl',
            subject: "Successful pipeline: ${currentBuild.fullDisplayName}",
            body: "It lives! Here's some details: ${env.BUILD_URL}"
        }
    }
}
