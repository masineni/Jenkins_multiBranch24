node('master') 
    {
        stage('continuous download') 
        {
            git 'https://github.com/sunildevops77/maven.git'
        }
        stage('continuous build') 
        {
            sh 'mvn package'
        }
        stage('continuous deployment') 
        {
            sh 'scp  /home/ubuntu/.jenkins/workspace/dev_pipeline/webapp/target/webapp.war   ubuntu@172.31.43.34:/var/lib/tomcat8/webapps/qaenv.war'
        }
         stage('continuous testing') 
        {
            sh 'echo "Hello World"'
        }
        stage('continuous delivery') 
        {
            sh 'scp  /home/ubuntu/.jenkins/workspace/dev_pipeline/webapp/target/webapp.war   ubuntu@172.31.40.14:/var/lib/tomcat8/webapps/qaenv.war'
        }
        
}
