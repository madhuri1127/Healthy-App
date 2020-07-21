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
	
  stage('deploy1')
 {
  publishHTML (target: [
      allowMissing: false,
      alwaysLinkToLastBuild: false,
      keepAll: true,
      reportDir: 'coverage',
      reportFiles: 'localtest.html',
      reportName: "RCov Report"
    ])
 }





}
