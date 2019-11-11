pipeline {
   node {
      // Mark the code checkout 'stage'....
      stage('拉取代码'){
         git 'https://github.com/running-dinosaur/jenkins_pipeline_java_maven.git'
      }
   
      // Mark the code build 'stage'....
      stage('构建'){
         // Run the maven build
         sh "mvn clean package"
         step([$class: 'JUnitResultArchiver', testResults: '**/target/surefire-reports/TEST-*.xml'])
      }
   }
}
