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
                sh "sudo rm -rf /var/www/React-app"
                sh "sudo cp -r ${WORKSPACE}/build/ /var/www/my-app/"
            }
        }
    }
}
