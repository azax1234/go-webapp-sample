   pipeline {
        agent any
        tools{
            git "myGit"
            go "myGo"
        }
        environment {
            GO111MOUDLE='on'
        }

        stages {
            stage(DEV){
                steps{
                    git 'https://github.com/azax1234/go-webapp-sample.git'
                    //sh 'go test ./...'
                }

            }
            stage(BUILD){
                steps{
                   sh 'go build .'
                }

            }
            stage(RUN){
                steps{
                    echo "${HOME}"
                    echo "${WORKSPACE}"
                    sh '${WORKSPACE}/go-webapp-sample &'
                }

            }
        }
    }
