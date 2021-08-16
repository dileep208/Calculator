/* groovylint-disable-next-line CompileStatic */
pipeline {
    agent { label 'MASTER' }
   
        stages {
            stage('scm') {
                steps {
                    git branch: "master", url: 'https://github.com/dileep208/Calculator.git'
                //input message: 'Continue to the next stage? ', submitter: 'dileepaws, dileepazure'

                }
            }
            stage('build') {
                steps {

                        sh " mvn package "                    
                }
            } 
           
            
        }
       
}