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
            readFile encoding: 'Base64', file: 'package.json'
            echo env.BRANCH_NAME      
      }
   }
}
}   
