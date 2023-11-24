pipeline {
    agent any

    parameters{
        string(name: 'SPEC', defaultValue: "cypress/integration/**/**", description "Enter the script path that you want to execute")
        choice(name: 'BROWSER', choices: ['chrome', 'edge', 'firefox'], description "Choose the browser where you want to run scripts")



    }
    options{
        ansiColor('xterm')
    }
    stages{
        stage('Building'){
            echo 'Building the application'
        }
        stage('Testing'){
            steps{
                bat "npn i"
                bat "npx cypress run --browser ${BROWSER} --spec ${SPEC}"
            }
        }
        stage('Deploying'){
            echo "Deploy the application"
        }
    }
}