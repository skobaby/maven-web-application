pipeline{
  agent any 
  tools {
    maven "maven3.8.6"
  }  
  stages {
    stage('1GetCode'){
      steps{
        sh "echo 'cloning the latest application version' "
        git branch: 'feature', credentialsId: 'gitHubCredentials', url: 'https://github.com/skobaby/maven-web-application'
      }
    }
    stage('3Test+Build'){
      steps{
        sh "echo 'running JUnit-test-cases' "
        sh "echo 'testing must passed to create artifacts ' "
        sh "mvn clean package"
      }
    }
    /*
    stage('4CodeQuality'){
      steps{
        sh "echo 'Perfoming CodeQualityAnalysis' "
        sh "mvn sonar:sonar"
      }
    }
    stage('5uploadNexus'){
      steps{
        sh "mvn deploy"
      }
    } 
    stage('8deploy2prod'){
      steps{
       deploy adapters: [tomcat8(credentialsId: 'tomcat credentials', path: '', url: 'http://3.98.142.64:8080/')], contextPath: null, war: 'target/*war'
      }
    }
}
  post{
    always{
      emailext body: '''Hey guys
Please check build status.
Thanks
Skobaby
+1 416 731 2250''', recipientProviders: [buildUser(), developers()], subject: 'success', to: 'mastercard-team@gmail.com'
    }
    success{
      emailext body: '''Hey guys
Good job build and deployment is successful.
Thanks
Skobaby 
+1 416 731 2250''', recipientProviders: [buildUser(), developers()], subject: 'success', to: 'master-card-team@gmail.com'
    } 
    failure{
      emailext body: '''Hey guys
Build failed. Please resolve issues.
Thanks
Skobaby 
+1 416 731 2250''', recipientProviders: [buildUser(), developers()], subject: 'success', to: 'master-card-team@gmail.com'
    }
  }
  */
}
