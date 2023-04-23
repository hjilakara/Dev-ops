pipeline{
    
    tools{
        maven 'mymaven'
    }
    
    agent any
    
    stages{
        stage('Fetch the sourcecode'){
            steps{
                git 'https://github.com/Sonal0409/DevOpsClassCodes.git'
            }
        }
        
        stage('Compile the code'){
            steps{
                sh 'mvn compile'
            }
        }
        stage('Code review report'){
            steps{
                sh 'mvn pmd:pmd'
            }
        }
        
        stage('unit testing'){
            steps{
                sh 'mvn test'
            }
        }
        
        stage('package'){
            steps{
                sh 'mvn package'
            }
        }
    }
    
}
