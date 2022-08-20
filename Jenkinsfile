pipeline {
    agent any

   // tools {
        // Install the Maven version configured as "M3" and add it to the path.
      //  maven "M3"
   // }
  // environment {
  //     PATH = "/opt/homebrew/Cellar/maven/3.8.6/bin:$PATH"
  // }

    stages {
        stage("clone_code") {
            steps {
                git "https://github.com/Nagendra2255/JenkinsDemo.git"
                
            }
        }
    
   
        stage("build_code") {
            steps {
            withMaven(maven : 'Default_Maven3')
            {
                sh "mvn clean test"
                }
                
            }
        }
        stage("code_deploy") {
            steps {
                sh "mvn install"
                
            }
        }
    
    }
}
