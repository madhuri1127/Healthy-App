node
{
stage('read')
{
git "https://github.com/madhuri1127/trial"
 
}
 stage('package')
{
bat "mvn clean install"
}

stage('test')
{
bat "mvn test"
 
}
 stage('deploy')
 {
  bat 'ssh root@krish-poc-node3 sh("""/root/sam.sh""")'
  
 }
 
 





}
