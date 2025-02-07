pipeline
{
    agent any
stages{


stage ('build,upload')
{
steps {
    
        withDockerRegistry([credentialsId: "bqe", url: ""]){
sh 'docker build -t fazelshah/nodejs-docker-app:v1.${BUILD_NUMBER} .'
 sh 'docker push fazelshah/nodejs-docker-app:v1.${BUILD_NUMBER}'   

           
}
}
}
 stage ('Remove Container Images'){
            steps{
sh 'docker image rmi -f fazelshah/nodejs-docker-app:v1.${BUILD_NUMBER}
            }
        }

stage ('run image'){
steps{
sh 'docker run -itd -P --name nodejs-container fazelshah/nodejs-docker-app:v1.${BUILD_NUMBER}'
}
}
}



