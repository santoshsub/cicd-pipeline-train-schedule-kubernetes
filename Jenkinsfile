pipeline {
    agent any
   
    stages {
       
 stage('DeployToProduction') {
            when {
                branch 'master'
            }
            steps {
                    kubernetesDeploy(
                    kubeconfigId: 'kubeconfig',
                    configs: 'train-schedule-kube.yml',
                    enableConfigSubstitution: true
                )
            }
        }
    }
}
