pipeline {
    agent any

    stages {
        stage ('Compile Stage1') {

            steps {
                withMaven(maven : 'maven_3_5_0') {
                    sh 'mvn clean compile'
                }
            }
        }

        stage ('Testing Stage2') {

            steps {
                withMaven(maven : 'maven_3_5_0') {
                echo "This is jenkins job"
                }
            }
        }


        stage ('Deployment Stage3') {
            steps {
                withMaven(maven : 'maven_3_5_0') {
                    sh 'mvn deploy'
                }
            }
        }
    }
}
