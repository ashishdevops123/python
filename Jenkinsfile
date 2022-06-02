pipeline{
    agent{ label 'build_pipeline' }
    triggers{ cron '0 * * * *'}
    stages{
        stage( 'checkout' ){
            steps{
                git url: 'https://github.com/ashishdevops123/python.git',
                    branch: 'master'

            }
        }
        stage('build'){
            steps{
                sh 'pip install -r requirements.txt'
            

            }
        }
        stage('test'){
            steps{
                sh 'tox -e py'
            }
        }
    }

}