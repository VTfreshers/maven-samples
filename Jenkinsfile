pipeline{
  agent any
        stages ("fetch")
        {
                steps
                {
                    echo ('fetching the source code')
                }
        }              
        stage ("test")
        {
        parellel
            stages ('test1')
            {
                steps
                 {
                    echo ('test1')
                 }
            }
            stages ('test2')
            {    
                steps
                 {
                    echo ('test2')
                 }
            }
        }
          stage ('deploy')
         {
                  steps
                  {
                      echo ('deploying stage')
                  }
         }
    
}     
