pipeline{
  agent any
  stages{
        stage ("fetch")
        {
                steps
                {
                    echo ('fetching the source code')
                }
        }              
        stage ("test")
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
}     
