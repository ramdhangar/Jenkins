node {
   stage('SCM Checkout') {
  git 'https://github.com/anup03gupta/webapp.git'

}
   stage('Build') {
     def mvn_version = 'maven'
      withEnv( ["PATH+MAVEN=${tool mvn_version}/bin"] ) {
      sh "$MAVEN clean package"
}
}
    stage('Package-Deploy') {
   sshagent(['pipe']) {
   sh 'scp -o StrictHostKeyChecking=no target/*.war ec2-user@172.31.36.70:/var/lib/tomacat8/webapps/'
}
}



}
