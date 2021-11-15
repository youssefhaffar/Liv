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
