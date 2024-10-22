pipeline {
     agent any
     stages {
        stage("Build") {
            steps {
                sh "sudo npm install"
                sh "sudo ng build"
            }
        }
        stage("Deploy") {
            steps {
                sh "sudo rm -rf /var/www/my-app"
                sh "sudo cp -r ${WORKSPACE}/build/ /var/www/my-app/"
            }
        }
    }
}
