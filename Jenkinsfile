pipeline {
    agent any 
    stages {
        stage("build"){
            steps {
                script {
            sh """
            aws ecr get-login-password --region ap-southeast-1 | sudo docker login --username AWS --password-stdin 315073111691.dkr.ecr.ap-southeast-1.amazonaws.com/micro-froentend
            docker build -t froentend:latest .
            docker run -d -p 1008:80 froentend

            """
        }
         }
    }
}
}
