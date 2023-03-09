pipeline {
    agent any

    stages {
        stage ('Compile Stage') {

            steps {
                
                    sh 'mvn clean compile'
                }
            
        }

        stage ('Testing Stage') {

            steps {
                
                    sh 'mvn test'
                }
            
        }


        stage ('Install Stage') {
            steps {
                
                    sh 'mvn install'
                    sh 'yum install tree -y'
                    sh 'yum remove tree'
                }
            
        }
        
        stage ('Echo Branch') {

            steps {
                
                    echo "This is test branch"
                }
            
        }
    }
}
