node('ubuntu') {
    stage('checkout'){
        git 'https://github.com/Bhuvana0509/spring-petclinic.git'
    }
    stage('package'){
        sh 'mvn package'
    }
    stage('Archive artifacts'){
        archiveArtifacts 'target/spring-*.jar'
    }
    stage('Publish JUnit reports'){
        junit 'target/surefire-reports/*.xml'
    }
}
