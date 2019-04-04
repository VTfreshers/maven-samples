pipeline{
  agent any
        stage ("fetch")
        {
                steps
                {
                    echo ('fetching the source code')
                }
        }              
        stages ("test")
        {
        parellel
            stage ('test1')
            {
                steps
                 {
                    echo ('test1')
                 }
            }
            stage ('test2')
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
