

pipeline {
  agent {
   node{
    label 'workstation'
   }
  }

   parameters {
          string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')

  }

  triggers { pollSCM('H/2 * * * *') }

  options {
    ansiColor('xterm')
  }
  environment{
    example_url = "example.com"
  }
  stages{
    stage ('one'){
     steps{
       sh 'echo hello world'
       sh 'echo ${example_url}'
       sh 'echo person -${PERSON}'
     }
    }
   }
  post{
    always{
       sh  'echo post cleanup step'

     }
    }
  }


