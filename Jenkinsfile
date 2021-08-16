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
             stage('SONAR ANALYSIS') {
                steps {
                    withSonarQubeEnv('SONAR-8.9LTS') {
                        // Requires SonarQube Scanner for Maven 3.2+
                        sh 'mvn org.sonarsource.scanner.maven:sonar-maven-plugin:3.2:sonar'

                    }
                }
                
            } 
           
            
        }
       
}