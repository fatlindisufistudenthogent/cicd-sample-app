node {
        stage('Preparation') {
            catchError(buildResult: 'SUCCESS') {
                sh 'docker stop samplerunning'
                sh 'docker rm samplerunning'
            }
        }
        stage('Build') {
            build 'BuildSampleApp-Fatlind'
        }
        stage('Results') {
            build 'TestSampleApp-Fatlind'
        }
    }