pipeline{
   agent any
    stages{
        stage('gitclone'){
            agent any
            steps{
                git credentialsId: 'bc010765-2802-482d-8502-5f629f70228a', url: 'https://github.com/sreyaku/PythonApplication-jenkins.git'
            }
        }

        stage('Dockerizing '){
            steps{
                bat '''
                docker container stop php-app
            docker container rm php-app
            docker build -t php-app . 
             docker run -d p 80:3001 php-app 
            '''
        }
        }
         }
    }
