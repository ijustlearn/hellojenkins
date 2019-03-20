pipeline {
    agent any
    stages {
        stage('build') {
            steps {
                sh 'echo "hello world"'
                sh '''
                    echo "sadas"
                '''
            }
        }
        stage('example'){
            input{
                message "should me continue?"
                ok "yes,we should"
                submitter "alice,bob"
                parameters{
                    string(name:"PERSON", defaultValue:"mr jenkins", description: 'who should i say hello to ?')
                }
            }
            steps{
                echo "hello ${PERSON} ,nice to meet you ."
            }
        }
    }
}
