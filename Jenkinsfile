pipeline{
    agent any 
        stages{
            stage("build stage") {
                steps{
                    sh 'mvn -f warartifact/pom.xml clean package'
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
