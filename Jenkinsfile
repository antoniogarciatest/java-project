pipeline {
        agent any

        stages {
                stage('build'){
                        steps {
                                sh 'ant -f build.xml -v'
                        }
                }
        }
        post {
                failure {
                        emailext {
                                subject: "${env.JOB_NAME} [${env.BUILD_NUMBER}] Failed!"
                                body: "<p>test</p>"
                                to: "antonio.garcia@beeva.com"
                        }                                
                }                       
        }
}

