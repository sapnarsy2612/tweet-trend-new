pipeline {
    agent {
        node { 
            label 'maven'
        }
    }
    //Since maven is added to bash_profile we need to update env var PATH everytime we run pipeline
    environment {
        PATH = "/opt/apache-maven-3.9.6/bin:$PATH"
    }
    stages {
        stage('Build') {
            steps {
                sh 'mvn clean deploy'
            }
        }
    }
}
