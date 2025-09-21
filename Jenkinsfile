pipeline {
    agent { label 'jenkins_agent' }
    environment {
        KUBECONFIG = '/home/jenkins/.kube/config'
    }
    stages {
        stage('kubectl') {
            steps {
                sh 'kubectl version'
                sh 'kubectl apply -f secret.yaml'
                sh 'kubectl apply -f configmap.yaml'
                sh 'kubectl apply -f deployment.yaml'
                sh 'kubectl apply -f service.yaml'
            }
        }
    }
}