pipeline {
    agent any

     environment {
        MQSI_RUNTIME = "C:/Progra~1/IBM/IIB/10.0.0.12/server/bin"
        MQSI_TOOLS = "C:/Progra~1/IBM/IIB/10.0.0.12/tools"
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
