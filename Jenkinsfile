pipeline {
  agent any
  environment {
    DIRECTORY_PATH = "/Users/darren/Developer/Jenkins/SIT223-5.1P/source-code"
    TESTING_ENVIRONMENT = "5.2P"
    PRODUCTION_ENVIRONMENT = "Darren"
  }
  stages {
    stage("Build") {
      steps {
        echo "Fetch source code from directory path: ${env.DIRECTORY_PATH}"
        echo "Compile the code and generate any necessary artifacts."
      }
    }
    stage("Test") {
      steps {
        echo "Unit tests."
        echo "Integration tests."
      }
    }
    stage("Code Quality Check") {
      steps {
        echo "Check the quality of the code."
      }
    }
    stage("Deploy") {
      steps {
        echo "Deploy the application to a testing environment specified by the environment variable."
      }
    }
    stage("Approval") {
      steps {
        echo "Waiting on approval"
        sleep 10 //seconds
      }
    }
    stage("Deploy to Production") {
      steps {
        echo "Deploy the code to the production environment using the environment variable: ${env.PRODUCTION_ENVIRONMENT}"
      }
    }
  }
}
