

pipeline 
{
    agent any

    stages 
    {
       
        stage('Build') 
        {
            steps 
            { 
                sh 'cat temp.txt'
                sh "sed -i 's/sopra/akku/g' config.properties"
                sh 'cat temp.txt'
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
   
