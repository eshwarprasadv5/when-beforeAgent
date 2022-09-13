pipeline{
    agent none
    environment{
        DEPLOY_TO="dev"
    }
    stages{
        stage('Build'){
         agent{
             label 'slave1'
         }
         when{
             beforeAgent false
             environment name:"DEPLOY_TO", value:"prod"
         }
         steps{
             echo "Builded"
         }
        }
    }
}
