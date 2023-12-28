pipeline{
    agent any
    stages{
        stage('scm check out'){
            steps{
                
                git branch: 'test', url: 'https://github.com/lakshmilokeshhema/todaywebproject.git'
            }
        }
        stage('scm validate'){
            steps{
                
                sh 'mvn validate'
            }
        }
        stage('scm clean'){
            steps{
                
                sh 'mvn clean'
            }
        }
        stage('scm compile'){
            steps{
                
                sh 'mvn compile'
            }
        }
        stage('scm test'){
            steps{
                
                sh 'mvn test'
            }
        }
        stage('build artifact'){
            steps{
                
                sh 'mvn package'
            }
        }
        stage('artifact is storing into local repo .m2'){
            steps{
                
                sh 'mvn install'
            
                
                }
        }
  }     
    
    
}
