pipeline {
    agent any

        stages {
            stage("GetSource") {
                steps {
                    dir('C:/Progra~2/Jenkins/workspace/SourceCode') {
                        git 'https://github.com/sriharsha-at-git/IIB-App1.git'
                        bat 'echo "hi"'
                        bat 'pause 5'
                        bat 'call ${MQSI_RUNTIME}/mqsiprofile.cmd'
                        bat '${env.MQSI_RUNTIME}/mqsilist'
                        bat 'echo "done" '
                    }
            }
        }
    }
}
