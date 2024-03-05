// @Library('my-shared-library') _

pipeline{

    agent any 

    stages('git checkout'){

        stage{

            steps{
                script{

                    git branch: 'main', url: 'https://github.com/anjankdey18/devops_java_app.git'
                }
            }

        }

    }

}