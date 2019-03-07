node {

stage('Clone Repository')
{
checkout scm
}

stage('Show me the files'){
sh "ls -l"
}

stage('Build docker image and push image to DockerHub'){

sh "docker build -t beth:latest ."
}

stage('Docker login to hub and push the image'){
sh "docker login -u 'bosiro' -p 'Srmartha1218'"
sh "docker tag practical_2019:latest bosiro/practical_2019:latest"
sh "docker push bosiro/practical_2019:latest"
}

stage('Apply changes to the environment') {
sh "ls -l"
}


}
