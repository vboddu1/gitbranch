//def input= $(echo sh (script: 'cat package.json | jq .version ', , returnStdout:true).trim())
def input = $(cat package.json | jq .version )
pipeline {
   agent any
   stages {
      stage('git checkout') {
         steps {
            git branch: 'dev', credentialsId: '951b62cc-d20f-479b-8b47-5bad66dc97ac', url: 'https://github.com/vboddu1/gitbranch.git'
         }
      }
      stage('branch name') {
         steps {
            echo env.BRANCH_NAME
            echo input
      }
   }
}
}   
