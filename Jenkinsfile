pipeline
{
    agent any
stages{

stage ('build,upload and run image')
{
steps {
    {
        withDockerRegistry([credentialsId: "bqe", url: ""])
sh 'docker build -t fazelshah/nodejs-docker-app:v1.${BUILD_NUMBER} .'
 sh 'docker push fazelshah/nodejs-docker-app:v1.${BUILD_NUMBER}'   
sh 'docker run -itd -P --name nodejs-container fazelshah/nodejs-docker-app:v1.${BUILD_NUMBER}'
}
}
}

}





}
