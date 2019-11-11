pipeline {
   agent any
   stages {
      // Mark the code checkout 'stage'....
      stage('拉取代码'){
         steps {
            git 'https://github.com/running-dinosaur/jenkins_pipeline_java_maven.git'
         }
      }
   
      // Mark the code build 'stage'....
      stage('构建'){
         steps {
            // Run the maven build
            sh "mvn clean package"
            junit '**/target/surefire-reports/TEST-*.xml'
         }
      }
   }
}
