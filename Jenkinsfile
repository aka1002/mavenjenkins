

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
           when {
                branch 'master'
                environment name: 'Test', value: 'any'
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
   
