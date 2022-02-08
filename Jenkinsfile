#!/usr/bin/env groovy

pipeline 
{
    agent any

    stages 
    {
       
        stage('Build') 
        {
            steps 
            { 
                bat 'get-content config.properties'
                //bat "sed -i 's/sopra/akku/g' config.properties"
                //bat  'get-content config.properties'
                echo 'Build App'
            }
        }
        stage('Test') 
        { 
           agent {
                label "some-label"
            }
            when {
                beforeAgent true
                branch 'production'
            }
//            when {
//                 branch 'master'
//             }
                 
            
//             input {
//                 message "want to test?"
//                 id "test"
//             }
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
   
