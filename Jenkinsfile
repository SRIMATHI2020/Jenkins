pipeline {
    agent any
      
      environment {
        ENV_URL         = "Pipeline.google.com"
          AN_ACCESS_KEY = credentials('SSH_CRED')
      }
    stages {

       stage("Stage One") {

           steps {
                echo "This is stage One"

                sh '''
                      echo DevOps Training
                      echo AWS Training
                      echo Name of the URL is ${ENV_URL}
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
                echo "This is stage Three"
           }
       }
    }
}