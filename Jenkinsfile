pipeline {
    agent {
        label 'macos'
    }

    stages {
	stage('git'){
        steps{
            checkout scm
        }
	}
        stage('Build') {
            steps {
                //sh ' # in our example, the project is not in the root of the repository'
                sh 'xcrun cd Example && xcodebuild -workspace BugfenderExample.xcworkspace -scheme BugfenderExample -sdk iphoneos CODE_SIGN_IDENTITY="" CODE_SIGNING_REQUIRED=NO'
            }
        }
    }
}


