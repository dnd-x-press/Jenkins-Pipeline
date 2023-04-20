pipeline {
  agent any
  environment {
    DIRECTORY_PATH = 'C:\\T1 2023\\SIT223\\SIT753 Week 5\\J Works'
    TESTING_ENVIRONMENT = 'Jenkins'
    PRODUCTION_ENVIRONMENT = 'Dash Nunes'
  }
  stages {
    stage('Build') {
      steps {
        echo "Fetch the source code from the directory path $DIRECTORY_PATH"
        echo "Compile the code and generate any necessary artifacts"
      }
    }
    stage('Test') {
      steps {
        echo "Run unit tests and integration tests"
      }
    }
    stage('Code Quality Check') {
      steps {
        echo "Check the quality of the code"
      }
    }
    stage('Deploy') {
      steps {
        echo "Deploy the application to $TESTING_ENVIRONMENT"
      }
    }
    stage('Approval') {
      steps {
        sleep 1
      }
    }
    stage('Deploy to Production') {
      steps {
        echo "Deploy the code to the production environment using $PRODUCTION_ENVIRONMENT"
      }
      post{
        success{
          mail to: "duchelle.nunes@gmail.com",
          subject: "IGNORE:Deployment stage status",
          body: "Deployment was Successfull"
        }
      }
    }
  }
}

