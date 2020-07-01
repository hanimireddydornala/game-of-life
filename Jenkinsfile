 pipeline{
	agent{label 'MASTER'}
		triggers{
			upstream(upstreamProjects: 'dummy', threshold: hudson.model.result.SUCCESS)
		}
		stages{
			stage('source'){
				steps{
					git url:'https://github.com/hanimireddydornala/game-of-life.git'
				}
			}
			stage('package'){
				steps{
					sh 'mvn package'
				}
				
			}
		}
	
 }