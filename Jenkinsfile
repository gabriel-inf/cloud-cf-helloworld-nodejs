@Library('piper-lib-os@v1.35.0') _
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
