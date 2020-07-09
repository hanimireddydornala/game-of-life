pipeline {
    agent any
	triggers {
	   upstream(upstreamProjects: 'dummy', threshold: hudson.model.Result.SUCCESS)
	}
    stages {
        stage('Source'){
            steps {
                git 'https://github.com/hanimireddydornala/game-of-life.git' 
            }
        }
        stage('Package'){
            steps {
                sh 'mvn package'
		    input 'Continue to next step?'
		    archiveArtifacts 'target/*.jar'
            }
        }
    }
}
