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
                    // sh 'cd /var/lib/jenkins/workspace/go_full_pipeline && go-webapp-sample &'
                }

            }
        }
    }
