pipeline {

     agent any

     stages {

        stage('Clone Repo') {
 
            steps {
                sh ' rm -rf jenRepo'
                sh 'git clone https://github.com/yurei14/jenRepo.git'
            }
        }
      
        stage('Run python file') {
           
           steps {
 
              sh 'python main.py'
           }
        }
     }
}

                           
