pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/khanmohsin40/terraform-eks-nodegroup-project-2.git'
            }
        }
    
        stage ("terraform init") {
            steps {
                sh ("terraform init -reconfigure") 
            }
        }
        
        stage ("plan") {
            steps {
                sh ('terraform plan') 
            }
        }

        stage (" Action") {
            steps {
                echo "Terraform action is --> ${action}"
                sh ('terraform ${action} --auto-approve') 
           }
        }
    }
}
