pipeline {
    agent any
      
      environment {
        ENV_URL = "Pipeline.google.com"
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

           steps {
                echo "This is stage Two"
                echo Name of the URL is ${ENV_URL}
           }
       }
       stage("Stage three") {

           steps {
                echo "This is stage Three"
           }
       }
    }
}