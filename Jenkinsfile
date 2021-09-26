pipeline {
      tools{
        maven 'MAVEN'
    }
    agent {label 'slave'}//to run on jenkins slave
    stages {
        stage('clone') {
            steps {
        git 'https://github.com/jglick/simple-maven-project-with-tests.git'
}
}
       stage('build'){
           steps{
            sh 'mvn -Dmaven.test.failure.ignore=true clean package'
           }
       }

}
}
