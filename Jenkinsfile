pipeline{
    agent any 
    stages{
        stage('stage1'){
            steps{
                echo 'Stage1'               
            }
        }
        stage('Docker Dev'){
            steps{
                sh 'docker build -t myimage:latest -f Dockerfile.dev .'            
            }
        }
        stage('Docker Test'){
            steps{
                sh 'docker run -e CI=true myimage:latest npn run test -- --coverage'            
            }
        }
        
    }
}
        
        //docker build -t MYIMAGE -f Dockerfile.dev .
        //dockerfile{
        //    filename 'Dockerfile.dev'
         //   additionalBuildArgs '-t MYIMAGE'
       // }
