@Library('jenkins-shared-library') _

pipeline{

    agent any

    parameters{
        choice(name: 'action', choices: 'create\ndelete', description: 'Choose create/Destroy')
    } 

    stages{

        stage('git checkout'){
            when { expression { params.action == 'create' }}
            steps{
                gitCheckout(
                    branch: "main",
                    url: "https://github.com/anjankdey18/devops_java_app.git"
                )
            }
        }

        stage('Unit test maven'){
            when { expression { params.action == 'create' }}
            steps{
                script{
                    mvnTest()
                }
            }
        }

        stage('Integration test maven'){
            when { expression { params.action == 'create' }}
            steps{
                script{
                    mvnIntegrationTest()
                }
            }
        }

        stage('Static code analysis: Sonarqube'){
            when { expression { params.action == 'create' }}
            steps{
                script{
                    staticCodeAnalysis()
                }
            }
        }
    }
}