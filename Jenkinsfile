pipeline {
	agent any
	stages {
		stage('Upload to AWS') {
			withAWS(region:'us-west-2') {
				    withAWS(credentials:'aws-static') {
    					s3Upload(file:'index.html', bucket:'jenkins-mys3', path:'./index.html')
			steps {
				sh 'echo "Hello World"'
				sh '''
				      echo "Multiline shell steps works too"
				      ls -lah
				'''
			}
				}
				}
		}
	}
}
