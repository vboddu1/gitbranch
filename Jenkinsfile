//def input= $(echo sh (script: 'cat package.json | jq .version ', , returnStdout:true).trim())
pipeline {
   agent any
   stages {
      stage('branch name') {
         environment {
      input = sh (script : "cat package.json|jq .version", returnStdout:true)
   }
         steps {
            echo env.BRANCH_NAME
            echo "${env.input}"
      }
   }
}
}   
