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
 junit allowEmptyResults: true, keepLongStdio: true, testDataPublishers: [[$class: 'JUnitFlakyTestDataPublisher']], testResults: ''
}
 





}
