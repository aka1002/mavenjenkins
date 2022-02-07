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

        stage('deploy') 
        {
            steps 
            {
                input 'Ready to go?     Proceed or Abort'
            }
        }

    }
}
   
