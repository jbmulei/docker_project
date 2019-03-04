node {

stage('Clone Repository')
{
checkout scm
}

stage('Show me the files'){
sh "ls -l"
}

stage('Build docker image'){

sh "docker build -t docker_test:latest ."
}

stage('Docker login to hub and push the image'){
sh "docker login -u 'jbmulei' -p 'Academy@2019' "
sh "docker tag docker_project:latest jbmulei/docker_project:latest"
sh "docker push jbmulei/docker_project:latest"
}

stage('Apply changes to the environment') {
sh "ls -l"
}


}
