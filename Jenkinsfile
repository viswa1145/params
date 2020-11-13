pipeline {
  agent any

  parameters {
    string(name: 'environment_name', description: 'Environment to deploy into')
    string(name: 'namespace', defaultValue: '', description: 'Namespace to deploy (leave empty for all namespaces)')
    string(name: 'shell_command', defaultValue: '', description: 'commad do you want run')
  }

  environment {
    ENVIRONMENT_NAME = "${params.environment_name}"
    SHELL_COMMAND = "${params.shell_command}"
  }

  stages {
    stage('Print environment name') {
      steps {
        echo "Will deploy to ${params.environment_name}"
      }
    }
   }
}
