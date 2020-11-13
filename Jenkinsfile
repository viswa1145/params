pipeline {
  agent any

  parameters {
    string(name: 'environment_name', description: 'Environment to deploy into')
    string(name: 'namespace', defaultValue: '', description: 'Namespace to deploy (leave empty for all namespaces)')
    string(name: 'shell_command', defaultValue: '', description: 'commad do you want run')
  }


  stages {
    stage('Print environment name') {
      steps {
        echo "Will deploy to ${params.environment_name}"
        //echo "Will deploy to ${params.environment_name}" >> {env.WORKSPACE}/file.groovey
        sh "cat /var/lib/jenkins/param/python.py|${params.shell_command}"
        //sh 'cat {env.WORKSPACE}/file.groovey'
      }
    }
   }
}
