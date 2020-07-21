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
		echo 'helloo'
	}
}

stage('test')
{
sh "mvn test"
 
}
 
 stage('deploy')
 {
 
  "sh /root/sam.sh "
  
 }
 





}
