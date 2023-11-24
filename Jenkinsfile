pipeline {
    agent any

    //  parameters{
    //     string(name: 'SPEC', defaultValue: "cypress/e2e/**/**", description "Enter the script path that you want to execute")
    //     choice(name: 'BROWSER', choices: ['chrome', 'edge', 'firefox'], description "Choose the browser where you want to run scripts")



    // }
    // options{
    //     ansiColor('xterm')
    // }
    stages{
        stage('Building'){
            steps{
                echo 'Building the application'
            }
        }
        stage('Testing'){
            steps{
                bat "npm i"
                bat "npx cypress run --spec cypress/e2e/1-getting-started/todo.cy.js"
            }
        }
        stage('Deploying'){
            steps{
                echo "Deploy the application"
            }
        }
    }
}