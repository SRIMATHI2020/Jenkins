pipeline {
    agent any
      
      environment {
        ENV_URL         = "Pipeline.google.com"
          AN_ACCESS_KEY = credentials('SSH_CRED')
      }

    parameters {
        string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
        text(name: 'BIOGRAPHY', defaultValue: '', description: 'Enter some information about the person')
        booleanParam(name: 'TOGGLE', defaultValue: true, description: 'Toggle this value')
        choice(name: 'CHOICE', choices: ['One', 'Two', 'Three'], description: 'Pick something')
        password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')
    }
    stages {
       stage('Parallel stages'){
          parallel {
              stage('In Parallel-1'){
                     steps {
                        echo "In Parallel 2"
                        sleep 15
                     }
              }
          }
       }
       stage("Stage One") {
           steps {
                echo "This is stage One"
                sh '''
                      echo DevOps Training
                      echo AWS Training
                      echo Name of the URL is ${ENV_URL}

                      env
                '''
           }
       }
       stage("Stage two") {
          environment {
             ENV_URL = "maths.google.com"
          }
           steps {
                echo "This is stage Two"
                echo "Name of the URL is ${ENV_URL}"
                echo "Name of the local URL is ${ENV_URL}"
           }
       }
       stage("Stage three") {
           steps {
                sh '''
                    echo "This is stage Three"
                    echo -e "\\e[32m Hai"
                '''
           }
       }
    }
}