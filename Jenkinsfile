
node 
{   
   stage('scm checkout') { 
      
      git 'https://github.com/devopsmastek/Auto.git'
     
     
   }
  
  
   stage ('deploy')
          {
    sh  "pwd"    
    def TARGET_IP = params.TARGET
    print "DEBUG: parameter foo = ${TARGET}"
             
           
    def source = "/var/lib/jenkins/workspace/autoscaling_project/*.html}"
//    def TARGET =  params.TARGET
//    sh "echo '$TARGET'"

         sshagent(['ubuntu']) {
        sh "scp -o StrictHostKeyChecking=no /var/lib/jenkins/workspace/autoscaling_project/*.html ubuntu@54.180.120.76:/var/www/html/"
                              }                    
                                       
        }
      
   }
