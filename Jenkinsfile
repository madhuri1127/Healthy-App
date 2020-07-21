node
{
stage('Checkout')
{
git "https://github.com/madhuri1127/trial"
 
}
 stage('Compile')
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

stage('Test')
{
sh "mvn test"
 
}
   stage('deploy')
 {
  sh './sam.sh'
 }

	
  stage('Html report generation')
 {
  publishHTML (target: [
      allowMissing: false,
      alwaysLinkToLastBuild: false,
      keepAll: true,
	   reportDir: './',
      reportFiles: 'localtest.html',
      reportName: "RCov Report"
    ])
 }
	
 stage('Test vulnerability')
 {
  if(false)
	 {
		 echo 'success'
	 }
	 else
	 {
		 sh "exit 1"
	 }
 }




}
