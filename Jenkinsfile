pipeline
{
    agent any
stages{

stage ('build image')
{
steps {
sh 'docker build -t fazelshah/nodejs-docker-app:v1.${BUILD_NUMBER} .'
sh 'docker run -itd -P fazelshah/nodejs-docker-app:v1""$BUILD_Number""'
}
}


}





}
