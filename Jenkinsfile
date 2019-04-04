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
