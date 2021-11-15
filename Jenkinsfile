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
      sh "sudo -S ansible-playbook ansible/build.yml -i ansible/inventory/host.yml "
            }
          }
                } 
        }
}
