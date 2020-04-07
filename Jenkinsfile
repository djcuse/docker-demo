node {
    // Get Artifactory server instance, defined in the Artifactory Plugin administration page.
    def server = Artifactory.server "deploy"
    // Create an Artifactory Maven instance.
    def rtMaven = Artifactory.newMavenBuild()
    def buildInfo
  
    
 rtMaven.tool = "maven"

    stage('Clone sources') {
        git url: 'https://github.com/djcuse/docker-demo.git'
    }

stage ('Build App') {


nodejs('nodejs') {
   sh "npm install"
}
sh "docker build -t mukesh1218/edison-devops-nodejs-webapp"
sh "docker push mukesh1218/edison-devops-nodejs-webapp"

  }
}
