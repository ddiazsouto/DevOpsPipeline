pipeline {
    agent any

    // environment{
    //         DATABASE_CREDENTIALS = credentials("CREDENTIALS")
    //         PASSWD = credentials("PASSWD")
            
    // }            PROBABLY NOT NECESSARY FOR FINAL PROJECT

    stages{

        // stage('Stage 0: Test'){
        //     steps{
               
        //         sh "bash testing.sh"             MAY NOT BE REQUIRED

        //     }
        // }

        stage('Stage 1: Build'){
            steps{

                sh "docker ps"
                

            }
        }

        stage('Stage 2: Push'){
            steps{
                
                sh " docker images"         // TO BE SET UP AND SINCRONIZER WITH DOCKERHUB
                
              
            }                                            
        }
        stage('Stage 3: Config'){
            steps{                                  // NEEDS ANSIBLE

                sh "docker run nginx"
            }
        }


        stage('Stage 4: Deploy'){                        //     TO BE DONE
            steps{

                sh "docker stack deploy --compose-file docker-compose.yaml Sentencer"
                
            }
        }
    }
}