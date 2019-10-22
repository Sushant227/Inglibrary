node('master'){
   
   stage('git checkout'){
                  git 'https://github.com/GayathriDevops/Inglibrary.git'
              }
   stage('java build'){
             sh '/opt/maven/bin/mvn clean deploy sonar:sonar'
         }

   stage('Running java backend application'){
             sh 'export JENKINS_NODE_COOKIE=dontKillMe ;nohup java -Dspring.profiles.active=sit -jar $WORKSPACE/target/*.jar &'
         }
}
