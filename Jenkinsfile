pipeline{
    agent any
    
    stages{

        stage("Build"){

            steps{
                
                echo "Building project"

            }

        }
    
        stage("Test"){
            when{
                expression{
                    
                    BRANCH_NAME == 'main'
                    
                }
            }
            
            steps{
                
                echo "Testing project"
                
            }
          
        }
    
        stage("Deploy"){
        
            steps{
                
                echo "Deploying project"
            }
        }
    
    }
}
