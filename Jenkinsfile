pipeline {
    agent { node { label 'AGENT-1' } } 

    stages {
        stage('Get version'){
            steps{
                script{
                    def packageJson = readJSON(file: 'package.json')
                    packageVersion = packageJson.version
                    echo "version: ${packageVersion}"
                }
            }
        }
        
        
    }

    post{
        always{
            echo 'cleaning up workspace'
            //deleteDir()
        }
    }
}