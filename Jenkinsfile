node
{
stage('Read SCM from GIT')
{
git "https://github.com/madhuri1127/Healthy-App"
 
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
	

	
	
	publishCoverage adapters: [jacocoAdapter('target/site/jacoco/jacoco.xml')]
	 publishHTML (target: [
      allowMissing: false,
      alwaysLinkToLastBuild: false,
      keepAll: true,
	   reportDir: 'target/site/jacoco',
      reportFiles: 'index.html',
      reportName: "Code Coverage Report"
    ])
	
 
}
 
stage('ZAP Security Scan')
 {
	
	
	 
  sh './sam.sh'
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
	 sh './a.sh'

	 value = readFile('foo.txt').trim()
  
	
echo value
	 
  if(value =="PASS")
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
