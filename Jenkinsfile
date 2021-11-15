pipeline
{
 agent any
  stages{
   stage('pull'){
    steps{
     scripts{
      checkout([$class: 'GitSCM' , branches: [[name: '/*master']],
       userRemoteConfigs: [[
        credentialsId: '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',
        url: 'https://github.com/youssefhaffar/Liv.git']]])
            }
          }
                }
        }
}
