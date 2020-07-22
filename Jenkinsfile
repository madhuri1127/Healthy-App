node
{
stage('Read SCM from GIT')
{
git "https://github.com/madhuri1127/trial"
 
}
 stage('Compile Package')
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

stage('Test Code Coverage')
{
sh "mvn test"
 
}
 

	
	
  stage('Security Scan Report')
 {
  publishHTML (target: [
      allowMissing: false,
      alwaysLinkToLastBuild: false,
      keepAll: true,
	   reportDir: './',
      reportFiles: 'localtest.html',
      reportName: "Security Scan Report"
    ])
 }
	
 stage('Deployment Decision')
 {
	 
sh 'cat foo.txt >value'
	
echo value
	 
  if(value =="Success")
	 {
		 echo 'Success'
	 }
	 else
	 {
		 echo 'Review Required'
		 sh "exit 1"
	 }
 }




}
