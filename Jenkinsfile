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
                        bat 'cd IIB-App1' 
                        bat returnStdout: true, script: '''
                        echo "hi"
                        pause 5
                        call $MQSI_RUNTIME/mqsiprofile.cmd
                        $MQSI_RUNTIME/mqsiservice
                        echo "done" '''
                    }
            }
        }
    }
}
