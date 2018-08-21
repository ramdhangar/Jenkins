pipeline {
    agent any 
        
   
     stages {
        stage('Build') {
            steps {
                echo "Hello from Build"
            }
        }
        stage('Test') {
            steps {
                 echo "Hello from Test"
            }
        }
        stage('Deliver for development') {
            when {
                branch 'development' 
            }
            steps {
                
		 echo "Im from develop branch"
            }
        }
        stage('Deploy for production') {
            when {
                branch 'production'  
            }
            steps {
                echo "Im from production branch"
            }
        }
    }
}
