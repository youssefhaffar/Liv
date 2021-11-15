pipeline
{
 agent any
  stages{
   stage('pull'){
    steps{
     scripts{
      checkout([$class: 'GitSCM' , branches: [[name: '*/master']],
       userRemoteConfigs: [[
        credentialsId: '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',
        url: 'https://github.com/youssefhaffar/Liv.git']]])
            }
          }
                }
        }
}
