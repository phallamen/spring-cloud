pipeline{
agent any
stages{
  stage("init"){
    steps{echo "hi there"}
  }
  stage("Code Review"){
    steps{
      withSonarqubeEnv("sonarqube"){
        sh 'mvn clean package sonar:sonar'
      }
    }
  }
}
}
