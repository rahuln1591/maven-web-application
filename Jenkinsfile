node
{
    echo "GitHub BranhName ${env.BRANCH_NAME}"
    echo "Jenkins Job Number ${env.BUILD_NUMBER}"
    echo "Jenkins Node Name ${env.NODE_NAME}"
  
    echo "Jenkins Home ${env.JENKINS_HOME}"
    echo "Jenkins URL ${env.JENKINS_URL}"
    echo "JOB Name ${env.JOB_NAME}"
  
    properties([
    buildDiscarder(logRotator(numToKeepStr: '3')),
    pipelineTriggers([
        pollSCM('* * * * *')
    ])
  ])
    def mavenHome=tool name: "maven3.6.3"
    
    stage('checkout')
    {
        git branch: 'development', 
        credentialsId: 'ca6672ba-509e-40aa-b298-44ecf620badc', 
        url: 'https://github.com/rahuln1591/maven-web-application.git'
        
    }
/*
    stage('ExecuteSonarcubeReport')
    {
        sh "${mavenHome}/bin/mvn sonar:sonar"
    }
    
    stage('Build')
    {
        sh "${mavenHome}/bin/mvn clean package"
    }
    
    stage('UploadArtifact')
    {
        sh "${mavenHome}/bin/mvn clean deploy"
    }
    
    stage('DeployAppIntoTomcatServer')
    {
        sshagent(['8b43312a-b608-43f5-beb6-7e00e2e99edd']) 
        {
            sh "scp -o StrictHostKeyChecking=no target/maven-web-application.war ec2-user@13.233.92.65:/opt/apache-tomcat-9.0.29/webapps/"
        }
    }
    
    stage('sendEmailNotification')
    {
        emailext body: '''Build is over....
        
        
        Thanks ans regards
        Rahul''', subject: 'Build is Over', to: 'rahul.n1591@gmail.com'
    }
    */
}
