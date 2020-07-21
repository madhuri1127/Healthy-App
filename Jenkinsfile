node
{
stage('read')
{
git "https://github.com/madhuri1127/trial"
 
}
 stage('package')
{
if(true)
	{
 sh "mvn clean install"

	}
	else
	{
		echo 'hellooooo'
	}
}

stage('test')
{
sh "mvn test"
 
}
 
 stage('deploy')
 {
 
  "sh /root/sam.sh "
pushToCloudFoundry cloudSpace: '', credentialsId:'', organization:'' , target:''
  
 }
 





}
