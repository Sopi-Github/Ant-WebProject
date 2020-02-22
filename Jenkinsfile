pipeline
    {
	  agent any
	  stages
	     {
		   stage ('scm checkout')
		     {
			   steps {
						git branch: 'master', url: 'https://github.com/Sopi-Github/Ant-WebProject.git'
				     }
			  }
		   stage ('prepare')
		   {
		       steps {
			        withAnt(installation: 'localant', jdk: 'localjdk-1.8') {
                    sh 'ant prepare'
				}			   
			   }
		   }
		    stage ('compile')
		     {
			     steps {
				     withAnt(installation: 'localant', jdk: 'localjdk-1.8') {
					     sh 'ant compile'
				     }
			     }   
		     }
		 }
    }
