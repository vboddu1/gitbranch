def input;
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
            withEnv(['input = cat package.json | jq .version']) 
            echo input
}
            echo env.BRANCH_NAME
            //output = readJSON text: version
            input = $(cat package.json| jq .version)  
      }
   }
}
}   
