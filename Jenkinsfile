pipeline {
  agent any

  environment {
    // FOO will be available in entire pipeline
    MQSI_RUNTIME = "C:\Progra~1\IBM\IIB\10.0.0.12\server\bin"
	MQSI_TOOLS = "C:\Progra~1\IBM\IIB\10.0.0.12\server\bin"
  }

  stages {
    stage("local") {
      environment {
        var = "STAGE"
      }
      steps {
        bat 'echo iibruntime = "$MQSI_RUNTIME"'
		bat 'echo iibtoolkit = "$MQSI_TOOLS"'
      }
    }
  }
}