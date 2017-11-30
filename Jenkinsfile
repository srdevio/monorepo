pipeline {
  // Have to use none as an agent so an input stage won't block anything
  agent none

  // Build the docker image using the Jenkins agent
  stages {
    stage('Load') {
      agent any
      steps {
        // From shared libs. Assumes SERVICE_NAME and REPO_NAME exist.
        pipeline = load 'pants/Jenkinsfile'
      }
    }
  }
}
