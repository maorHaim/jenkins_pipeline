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
		echo 'Another commit'
            }
        }

    }
    post{
            success{
                mail bcc: '', body: 'this time everything is good/ ', cc: '', from: '', replyTo: '', subject: ' successful build', to: 'maor.haim@gmail.com'
            }
            failure{
                mail bcc: '', body: 'this time everything is bad/ ', cc: '', from: '', replyTo: '', subject: 'Failed build', to: 'maor.>
            }
    }
}
