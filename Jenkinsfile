node {

stage('Clone Repository')
{
checkout scm
}

stage('Show me the files'){
sh "ls -l"
}

stage('Build docker image'){

sh "sudo docker build -t docker_test:latest ."
}

stage('Docker login to hub and push the image'){
sh "sudo docker login -u 'smbutha' -p 'Botha321' "
sh "sudo docker tag raspberry:latest smbutha/raspberry:latest"
sh "sudo docker push smbutha/raspberry:latest"
}

stage('Apply changes to the environment') {
sh "sudo ls -l"
}


}

