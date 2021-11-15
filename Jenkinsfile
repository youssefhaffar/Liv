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
   stage('npm intall'){
    steps{
     script{
      sh "sudo npm install"
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
                stage('docker'){
    steps{
     script{
      sh "sudo -S ansible-playbook ansible/docker.yml -i ansible/inventory/host.yml "
            }
          }
                }
                stage('dockerHub'){
    steps{
     script{
      sh "sudo -S ansible-playbook ansible/docker-registry.yml -i ansible/inventory/host.yml "
            }
          }
                }
        }
}
