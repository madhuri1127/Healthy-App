node
{
stage('read')
{
git "https://github.com/madhuri1127/trial"
 
}
 stage('package')
{
sh "mvn clean install"
}

stage('test')
{
sh "mvn test"
 
}
 stage('deploy')
 {
 sudo cd /root
 sudo ./sam.sh
  
 }
 
 





}
