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
                steps
                 {
                    echo ('test1')
                 }
                 steps
                 {
                    echo ('test2')
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
