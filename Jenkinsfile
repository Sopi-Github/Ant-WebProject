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
		   stage ('build')
		   {
		       steps {
			        withAnt(installation: 'localant', jdk: 'localjdk-1.8') {
                    sh 'ant build'
				}			   
			   }
		   }
		 }
    }
