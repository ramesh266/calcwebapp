node{
    stage('Git Clone'){
        git 'https://github.com/ramesh266/calcwebapp.git'
    }
    stage('Maven Package'){
        def mvnHome = tool name: 'Maven', type: 'maven'
        sh "${mvnHome}/bin/mvn package"
    }
    stage('Deployment'){ 
        sh 'cp target/*.war /home/ubuntu/opt/tomcat/webapps'
    }    
}
