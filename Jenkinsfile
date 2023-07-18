

pipeline {
agent {
  node{
   label 'workstation'
  }
 }
 environment{
   example_url = "example.com"
 }
 stages{
   stage ('one'){
   steps{
     sh 'echo hello world'
     sh 'echo ${example_url}
    }
   }
  }
  post{
  always{
 sh  'echo post cleenup step'

   }
  }
 }