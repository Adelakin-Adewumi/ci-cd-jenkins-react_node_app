pipeline {
     agent any
     stages {
        stage("Build") {
            steps {
                sh "sudo npm install"
                sh "sudo npm run build"
            }
        }
        stage("Deploy") {
            steps {
                sh "sudo rm -rf /var/www/aws-3-tier-mernapp-deployment"
                sh "sudo cp -r /var/lib/jenkins/jobs/build/ /var/www/aws-3-tier-mernapp-deployment/"
            }
        }
    }
}
