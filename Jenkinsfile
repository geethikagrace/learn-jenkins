

pipeline {
agent {
  node{
   lable 'workstation'
  }
 }
 stages{
   stage ('one'){
   steps{
     sh 'echo hello world'
    }
   }
  }
  post{
  always{
 sh  'echo post cleenup step'

   }
  }
 }