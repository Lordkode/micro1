pipeline {
    agent any
    stages {
        stage("Hello") {
            steps {
                echo "Hello World !"
            }
        }
        stage("for the fix branch"){
            when{
                branch 'fix/*'
            }
            steps{
                sh """
                    cat README.md
                """
            }
        }
        stage("for the PR"){
            when{
                branch 'PR-*'
            }
            steps{
                echo "This is a PR branch"
            }
        }
    }
}
 