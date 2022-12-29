pipeline {

     agent any

     stages {

        stage('Clone Repo') {
 
            steps {
                sh ' rm -rf <directory name>'( if you've previously cloned the repo on your machine)
                sh 'git clone <repo URL>'
            }
        }
      
        stage('Run python file') {
           
           steps {
 
              sh 'python main.py'
           }
        }
     }
}

                           
