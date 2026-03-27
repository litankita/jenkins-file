pipeline{
	agent any
		stages{
			parallel{
				stage('fetch the code')
				{
				    steps{
				    git 'https://github.com/litankita/mypipeline.git'
				    }
				}
				stage('install dependencies')
				{
                    steps{
                        sh '''sudo apt install apache2 -y
'''
}
				}
			}
				stage('deploy')
				{
				    steps{
				            sh 'sudo cp -R * /var/www/html'
				}
				}
		}
		post{
			success{
				script{
					mail bcc: '', body: 'it is a success', cc: '', from: '', replyTo: '', subject: '', to: 'sushreankita@gmail.com'
				}

			}
			failure{
				script{
						mail bcc: '', body: 'it is a failure', cc: '', from: '', replyTo: '', subject: '', to: 'sushreankita@gmail.com'
				}

			}
			always{
				script{
					mail bcc: '', body: 'my_pipeline is a executed', cc: '', from: '', replyTo: '', subject: '', to: 'sushreankita@gmail.com'
				}
			}

		}
}
