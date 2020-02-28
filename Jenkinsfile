properties([parameters([string(defaultValue: 'neha', description: '', name: 'NAME', trim: false), string(defaultValue: 'cybage', description: '', name: 'COMPANY', trim: false)])])
pipeline {
    agent any
    stages {
        stage('Parallel Stage') {
            parallel {
                stage('Parallel Test 1') {
                    steps {
                        build job: 'demo-job3', parameters: [string(name: 'NAME', value: String.valueOf(NAME)),string(name: 'COMPANY', value: String.valueOf(COMPANY))]
                        
                    }
                }
                stage('Parallel Test 2') {
                    steps {
                        build(job: "demo-job1")
                    }
                }
            }
        }
    }
}
