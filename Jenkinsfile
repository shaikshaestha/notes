pipeline {
    agent any 
    stages {
        stage ('hello') {
            steps {
                sh '''
                rm -rf *
                git clone https://github.com/shaikshaestha/notes.git 
                '''
            }
        }
        stage ('maven_clean') {
            
            steps {
                sh '''
                cd notes
                mvn clean
                '''
            }
        }
        
        stage ('maven_compile') {
            steps {
                sh '''
                cd notes
                mvn compile
                '''
            }
        }
        
       
        stage ('maven_test') {
            steps {
                sh '''
                cd notes
                mvn test install package
                '''
            }
        }
        
    }
}
