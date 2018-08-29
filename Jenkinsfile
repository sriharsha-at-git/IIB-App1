pipeline {
    agent any

    environment {
        // FOO will be available in entire pipeline
        MQSI_RUNTIME = "${env.MQSI_RUNTIME}"
        MQSI_TOOLS = "${env.MQSI_TOOLS}"
    }

        stages {
            stage("GetSource") {
                steps {
                    dir('C:/Progra~2/Jenkins/workspace/SourceCode') {
                        git 'https://github.com/sriharsha-at-git/IIB-App1.git'
                        bat 'echo "hi"'
                        bat 'pause 5'
                        bat 'call $MQSI_RUNTIME/mqsiprofile.cmd'
                        bat '$MQSI_RUNTIME/mqsilist'
                        bat 'echo "done" '
                    }
            }
        }
    }
}
