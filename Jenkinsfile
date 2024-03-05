@Library('jenkins-shared-library') _

pipeline{

    agent any 

    stages{

        stage('git checkout'){

            steps{
                gitCheckout(
                    branch: "main",
                    url: "https://github.com/anjankdey18/devops_java_app.git"
                )
            }
        }

        stage('Unit test maven'){

            steps{
                script{
                    mvnTest()
                }
            }
        }
    }
}