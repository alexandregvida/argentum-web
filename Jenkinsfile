pipeline {
    agent any
    tools { 
        maven 'MAVEN_HOME' 
        jdk 'JAVA_8' 
      }
    stages {
        stage ('Initialize') {
            steps {
                sh '''
                    echo "PATH = ${PATH}"
                    echo "M2_HOME = ${M2_HOME}"
                ''' 
            }
        }
        stage('Build') {
            steps {
                sh 'mvn clean package sonar:sonar' 
                echo 'Building1..'
                echo 'Building2..'
                echo 'Building3..'
                echo 'Building4..'


            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}