node{

def mavenHome = tool name: "maven3.9.5" 

//Checkout Stage
stage('CheckoutCode'){
  git branch: 'development', credentialsId: 'af39f694-8105-4ebd-9d60-db90181a2e58', url: 
'https://github.com/Rohanghodke1603/maven-web-application.git'
}

//Build Stage
stage('Build'){
sh "$mavenHome/bin/mvn clean package"
}
/*
//Generate SonarQube Report
stage('SonarQube Report'){
sh "$mavenHome/bin/mvn sonar:sonar"
}

//Upload Artifact into Artifactory repo
stage('UploadArtifactsIntoNexus'){
sh "$mavenHome/bin/mvn deploy"
}


//Deploy App into Tomcat Server
stage('DeployAppIntoTomcat'){
sshagent(['9d037e09-54aa-4870-b3fb-27d6f28f67aa']) {
sh "scp -o StrictHostKeyChecking=no target/maven-web-application.war ec2-user@15.206.27.252:/opt/apache-tomcat-9.0.86/webapps"
}
}
*/
}//Node Closing
