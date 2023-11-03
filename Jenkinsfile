pipeline {
    agent any
    stages {
        stage('NORMAL Stage') {
            steps {
                echo 'I am one'
            }
        }
        stage('Parallel Stage') {
            when {
                branch 'master'
            }
            failFast true
            parallel {
                stage('stage one') {
                    agent {
                        label "stageonebranch"
                    }
                    steps {
                        echo "Me in stage one"
                    }
                }
                stage('Stage two') {
                    agent {
                        label "stage two"
                    }
                    steps {
                        echo "Me in stage two"
                    }
                }
                stage('Stage three') {
                    agent {
                        label "Stage Three"
                    }
                }
            }
        }
    }
}
