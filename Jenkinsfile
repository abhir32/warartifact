pipeline{
    agent any 
        stages{
            stage("build stage") {
                steps{
                    sh 'mvn clean package'
                }
                post{
                    success {
                        echo "now archiving the artifacts..."
                        archiveArtifacts artifacts: '**/*.war'
                    }
                }
            }
        }

}
