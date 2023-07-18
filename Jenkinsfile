

//  pipeline {
//    agent {
//      node{
//       label 'workstation'
//       }
//      }
//
//      parameters {
//           string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
//            }
//
//      options {
//          ansiColor('xterm')
//       }
//      environment{
//          example_url = "example.com"
//       }
//
//
//     stages{
//         stage ('one'){
//             input {
//               message "Should we approve?"
//               ok "Yes"
//               }
//             steps{
//               sh 'echo hello world'
//               sh 'echo ${example_url}'
//               sh 'echo person -${PERSON}'
//              }
//         }
//
//         stage ('two'){
//         when{
//         expression{
//          GIT_BRANCH == "origin/test"
//         }
//         }
//             steps{
//               sh 'env'
//             }
//         }
//         }
//           post{
//              always{
//                sh  'echo post cleanup step'
//
//               }
//           }
//  }

pipeline{
    agent any

    stages{
        stage('parallel'){
          parallel {
              stage ('one'){
                  sh 'echo hello stage one'
              }
              stage ('two'){
                  sh 'echo hello stage two'
              }
              stage ('three'){
                  sh 'echo hello stage three'
              }

          }
        }

    }
 }






