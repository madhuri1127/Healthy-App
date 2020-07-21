pipeline {
	agent any 
	stages{

stage('read')
{
 steps{
  
git "https://github.com/madhuri1127/trial"

 }
}
 stage('package')
{
 when {
    
    expression { return false }
}
 steps{

 sh "mvn clean install"
 }

}

stage('test')
{
 steps
 {
sh "mvn test"
 } 
}
 
 stage('deploy')
 {
  step
  {
  "sh /root/sam.sh "
  }
  
 }
}

}




