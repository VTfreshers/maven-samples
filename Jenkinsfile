pipeline{
  agent any
  stages{
        stage ('fetch')
        {
                  steps
                  {
                    echo ("fetching the source code")
                  }
        }  
       stage ("Code Analysis")
			  {
			          	steps
				          {
					          sh label: '', script: '''mvn sonar:sonar \\
  -Dsonar.projectKey=VTfreshers_maven-samples \
  -Dsonar.organization=vtfreshers-github \
  -Dsonar.host.url=https://sonarcloud.io \
  -Dsonar.login=9bcdac8fa983cf077fa2c157896e755ad1d329fd
				          }
			  }
        stage ('test')
        {
        parallel
          {
            stage ('Atest:integration')
            {
                steps
                 {
                    echo ("integration")
                 }
            }
            stage ('Btest:fuctionality')
            {    
                steps
                 {
                    echo ("functionality")
                 }
            }
          }
        }  
          stage ('deploy')
         {
                  steps
                  {
                      echo ("deploying stage")
                  }
         }
                    
      }
}     
