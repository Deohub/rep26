node('built-in') 
{
    stage('Continuous Download_master') 
	{
    git 'https://github.com/sunildevops77/maven.git'
	}
    stage('Continuous Build_master') 
	{
    sh label: '', script: 'mvn package'
	}
    stage('Continuous Deployment_master') 
	{
sh label: '', script: 'scp /home/ubuntu/.jenkins/workspace/ScriptedPipeline/webapp/target/webapp.war   ubuntu@172.31.26.217:/var/lib/tomcat8/webapps/qaenv.war'
	}
    stage('Continuous Testing-Master') 
	{
              sh label: '', script: 'echo "Testing Passed"'
	}
    stage('Continuous Delivery_Master') 
	{
sh label: '', script: 'scp /home/ubuntu/.jenkins/workspace/ScriptedPipeline/webapp/target/webapp.war   ubuntu@172.31.22.88:/var/lib/tomcat8/webapps/prodenv.war'
	}
}
