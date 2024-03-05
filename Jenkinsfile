@Library('jenkins-shared-library') _

pipeline{

    agent any 

    stages{

        stage('git checkout'){

            steps{
                script{

                    gitCheckout{
                        branch: "main"
                        url: "https://github.com/anjankdey18/devops_java_app.git"
                    }

                }
            }

        }

    }

}