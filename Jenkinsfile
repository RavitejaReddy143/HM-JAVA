pipeline
 {
    agent any

    stages 
{
      
        stage ('Compile Stage') 
{

            steps
 {
               
                    sh 'mvn  clean install'
                
            }
        }

        stage ('Testing Stage')
 {

            steps
 {
                
                    sh 'mvn -f pom.xml test'
                }
            
        }
        stage('Deploy to Tomcat')
{
        steps
 {
        sh 'cp -R /var/lib/jenkins/workspace/declarativejob/target/* /opt/apache-tomcat-8.5.3/webapps/'
        }
        }


        
    }
}
