pipeline
{
 agent any
  stages{
   stage('Pull'){
    steps{
     script{
      checkout([$class: 'GitSCM' , branches: [[name: '*/master']],
       userRemoteConfigs: [[
        credentialsId: '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',
        url: 'https://github.com/youssefhaffar/Liv.git']]])
            }
          }
                }
        }
}
