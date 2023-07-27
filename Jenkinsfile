pipeline{
    agent any
    stages{
        stage ('SCM checkout'){
          steps{  
              git branch: 'main', url: 'https://github.com/awcharpratiksha/flask.git'
        }
        }
        stage ('docker image build'){
            steps{
                sh '/usr/bin/docker image build -t pratikshaawchar/pythonimage .'
            }
        }
        stage ('docker login'){
            steps{
                sh 'echo dckr_pat_ihLgk9pvG9HmLz97F_zUPOVWU2U | /usr/bin/docker login -u pratikshaawchar123 --password-stdin '
            }
        }    
        stage ('docker image push'){
            steps{
                sh '/usr/bin/docker image push pratikshaawchar123/pythonimage'
            }
        }
    }
}
