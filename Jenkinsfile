node {

stage('Clone Repository')
{
checkout scm
}

stage('Show me the files'){
sh "ls -l"
}

stage('Build docker image'){

sh "sudo docker build -t raspberry:latest ."
}

stage('Docker login to hub and push the image'){
sh "docker login -u 'smbutha' --password 'Botha321' "
sh "docker tag raspberry:latest smbutha/raspberry:latest"
sh "docker push smbutha/raspberry:latest"
}

stage('Apply changes to the environment') {
sh "ls -l"
}


}

