pipeline{
	agent any
		stages{
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
				stage('deploy')
				{
				    steps{
				            sh 'sudo cp -R * /var/www/html'
				}
				}
		}
}
