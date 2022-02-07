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
             when (BRANCH_NAME != 'master') 
            steps 
            {
                echo 'Build App'
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
   
