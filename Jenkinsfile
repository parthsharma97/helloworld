pipeline {
    agent any
     stages {
         stage('--clean--') {
            steps {
                try{
                    sh "mvn clean"
                    echo "Im not going to fail"
                    currentBuild.result = 'SUCCESS'
                    } catch (Exception err) {
                    currentBuild.result = 'FAILURE'
                  }
                echo "RESULT: ${currentBuild.result}"
               }
         }
         stage('--test--') {
            steps {
                try{
                    sh "mvn test"
                    echo "Im not going to fail"
                    currentBuild.result = 'SUCCESS'
                    } catch (Exception err) {
                    currentBuild.result = 'FAILURE'
                   }
                echo "RESULT: ${currentBuild.result}"
               }
         }
         stage('--package--') {
            steps {
                try{
                    sh "mvn package"
                    echo "Im not going to fail"
                    currentBuild.result = 'SUCCESS'
                    } catch (Exception err) {
                    currentBuild.result = 'FAILURE'
                   }
                echo "RESULT: ${currentBuild.result}"
               }
         }
         stage('--deploy--') {
            steps {
                try{
                    sh "mvn deploy"
                    echo "Im not going to fail"
                    currentBuild.result = 'SUCCESS'
                    } catch (Exception err) {
                    currentBuild.result = 'FAILURE'
                   }
                echo "RESULT: ${currentBuild.result}"
               }
         }
    }
}
