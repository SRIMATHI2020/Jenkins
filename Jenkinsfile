pipeline {
    agent any

    stages {

       stage("Stage One") {

           steps {
                echo "This is stage One"

                sh '''
                      echo DevOps Training
                      echo AWS Training
                '''
           }
       }
       stage("Stage two") {

           steps {
                echo "This is stage Two"
           }
       }
       stage("Stage three") {

           steps {
                echo "This is stage Three"
           }
       }
    }
}