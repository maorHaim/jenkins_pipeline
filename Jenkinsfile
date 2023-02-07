pipeline {
    agent any
    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
            }
        }
        stage('Goodbye'){
            steps {
                echo 'Goodbye'
            }
        }

    }
    post{
            success{
                mail bcc: '', body: 'this time everything is good/ ', cc: '', from: '', replyTo: '', subject: ' successful build', to: 'maor.haim@gmail.com'
            }
            failure{
                step([$class: 'Mailer', notifyEveryUnstableBuild: true, recipients: 'maor.haim@gmail.com', sendToIndividuals: false])
            }
    }
}
