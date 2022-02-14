pipeline {
    agent any
            
    stages {
        stage('Check') {
                steps {
                        echo 'Hi, How are you'		
                }
        }
	    stage('Clone'){
		    
		steps {
			sh'rm -rf testJenkins'
			checkout scm
			//sh 'git clone https://github.com/Asma22w/testJenkins.git'
        }
	    }
        stage('Run') {
		steps {
		 	
		  sh'sudo docker image build -t myapp .'
			
                  sh'sudo docker run -it -p 3000:3000 -d myapp'
			
		}
                      
        }
        
        }
    }
