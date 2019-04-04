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
        stage ('test')
        {
        parellel
          {
            stage ('test:integration')
            {
                steps
                 {
                    echo ("integration")
                 }
            }
            stage ('test:fuctionality')
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
