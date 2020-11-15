pipeline {


agent any


stages {

stage('Test') {


steps {


sh '/usr/local/bin/cfn-lint ./*.json'


}


}



stage('Deploy') {


steps {
  
sh "/usr/local/bin/aws cloudformation create-stack --stack-name ec2-git-Stage --template-body file://ec2.json --region 'ap-northeast-1'"


}


}
}
}
