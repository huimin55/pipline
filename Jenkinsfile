pipeline {
    agent any
    stages {
        stage("Build") {
            steps {
                echo "Building the project ......."  
            }
        }
        stage("Test") {
            steps {
                echo "Run Project Testing ...... "

                echo "Run Project testing....."
		echo "add ssh key"
            } 
	post {
		always {
		echo 'This will always run'
		}
		success {
		echo 'This will run only if successful'
		}
		failure {
		echo 'This will run only if failed'
		}
		unstable {
		echo 'This will run only if the run was marked as unstable'
		}
		changed {
	echo 'This will run only if the state of the Pipeline has changed'}	
        }
        stage("Deploy") {
            steps {
                echo "Deploying the project ........"
            }
        }
    }
}
