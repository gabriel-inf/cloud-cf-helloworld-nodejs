@Library('piper-lib-os') _
node() {
	stage('Test Stage') {
		echo 'Test Stage - Successfully' 
	}
	stage('prepare') {
		checkout scm
		setupCommonPipelineEnvironment script:this
	}
	stage('build') {
		mtaBuild script: this
	}
	
	stage('deploy') {
        cloudFoundryDeploy script: this
	}
}
