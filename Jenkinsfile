pipeline {
    agent any

     environment {
        MQSI_RUNTIME = "C:/Progra~1/IBM/IIB/10.0.0.12/server/bin"
        MQSI_TOOLS = "C:/Progra~1/IBM/IIB/10.0.0.12/tools"
    }
        stages {
            stage("GetSource") {
                step {
                    dir('C:/Progra~2/Jenkins/workspace/SourceCode') {
                        bat 'Downloading src"'
                        git 'https://github.com/sriharsha-at-git/IIB-App1.git'
                        bat 'download completed'
                    }
                }
                step {
                    dir('C:/Progra~2/Jenkins/workspace/SourceCode') {
                        bat 'call C:/Progra~1/IBM/IIB/10.0.0.12/server/bin/mqsiprofile.cmd'
                        bat 'C:/Progra~1/IBM/IIB/10.0.0.12/server/bin/mqsilist'
                    }
                }
            }
            stage("Initialize") {
                step {
                    dir('C:/Progra~2/Jenkins/workspace/SourceCode') {
                        bat 'call C:/Progra~1/IBM/IIB/10.0.0.12/server/bin/mqsiprofile.cmd'
                        bat 'C:/Progra~1/IBM/IIB/10.0.0.12/server/bin/mqsilist'
                    }
                }
            }
            stage("Compile") {
                step {
                    dir('C:/Progra~2/Jenkins/workspace/SourceCode') {
                       
                        bat 'C:/Progra~1/IBM/IIB/10.0.0.12/server/bin/mqsicreatebar -data . -b ./DEV-TEST.bar -a HTTP_JSON_WS_APP'
                    }
                }
            }
        }
}
