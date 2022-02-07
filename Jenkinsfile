def isValidationSuccess = true 

pipeline 
{
    agent any

    stages 
    {
       stage("Validate") {
        when {
            environment name: 'VALIDATION_REQUIRED', value: 'true'
        }
        steps {
            if(some_condition){
                isValidationSuccess = false;
            }
        }
    } 
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
            expression { isValidationSuccess == true }
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
   
