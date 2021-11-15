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
   stage('Build'){
    steps{
     script{
      sh "ansible-playbook ansible/build.yml -i ansible/inventory/host.yml "
            }
          }
                } 
        }
}
