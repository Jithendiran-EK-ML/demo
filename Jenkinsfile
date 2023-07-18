/*
 See the documentation for more options:
 https://github.com/jenkins-infra/pipeline-library/
*/
pipeline {
    agent any
    stages{
        stage('build') {
            steps{
            bat """
            call mvn spotless:apply 
            call mvn clean install
            """
            }
        }
        stage('branch') {
            steps{
                bat """
                call echo "%env.BRANCH_NAME%"
                """
            }
        }
    }
}
