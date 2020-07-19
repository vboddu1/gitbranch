//def input= $(echo sh (script: 'cat package.json | jq .version ', , returnStdout:true).trim())
pipeline {
   agent any
   stages {
      stage('git checkout') {
         steps {
            git branch: 'dev', credentialsId: '951b62cc-d20f-479b-8b47-5bad66dc97ac', url: 'https://github.com/vboddu1/gitbranch.git'
         }
      }
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
