pipeline {
    agent any

    environment {
        // FOO will be available in entire pipeline
        MQSI_RUNTIME = "C:/Progra~1/IBM/IIB/10.0.0.12/server/bin/"
        MQSI_TOOLS = "C:/Progra~1/IBM/IIB/10.0.0.12/tools/"
    }

        stages {
            stage("GetSource") {
                steps {
                    dir('C:/Progra~2/Jenkins/workspace/SourceCode') {
                        git 'https://github.com/sriharsha-at-git/IIB-App1.git'
                        bat 'echo "hi"'
                        bat 'pause 5'
                        bat 'call C:/Progra~1/IBM/IIB/10.0.0.12/server/bin/mqsiprofile.cmd'
                        bat 'C:/Progra~1/IBM/IIB/10.0.0.12/server/bin/mqsiservice'
                        bat 'echo "done" '
                    }
            }
        }
    }
}
