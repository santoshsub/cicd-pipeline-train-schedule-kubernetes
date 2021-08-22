pipeline {
    agent any
   
    stages {
       
 stage('DeployToProduction') {
            when {
                branch 'master'
            }
            steps {
                input 'Deploy to K8s?'
                milestone(1)
                kubernetesDeploy(
                    kubeconfigId: 'kubeconfig',
                    configs: 'train-schedule-kube.yml',
                    enableConfigSubstitution: true
                )
            }
        }
    }
}
