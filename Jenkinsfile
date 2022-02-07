

pipeline 
{
    agent any

    stages 
    {
       
        stage('Build') 
        {
            steps 
            {
                echo 'Build App'
            }
        }
        stage('Test') 
        {
           
                beforeInput true
                 
            
            input {
                message "want to test?"
                id "test"
            }
            steps 
            {
                echo 'Test'
            }
        }

        stage('deploy') 
        {
            steps 
            {
                input 'deploy to QA ?     Proceed or Abort '
                
                   
                
            }
        }

    }
}
   
