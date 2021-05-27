// Quick start declarative pipeline for Python
pipeline {
    agent {
        docker {
            image 'python:3.5.1'
            }
        }
    environment {
        ENV_VAR = 'globaal'
        GLB_INT = 14
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

        stage('final check') {
            steps {
                input "No need for nerves, we can still go back. Proceed anyway?"
            }
        }

        stage('deploy') {
            steps {
                echo 'placeholder while we build a real deployment step'
            }
        }
    }
}
