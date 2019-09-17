node{
    stage 'Checkout'
    git url: 'https://github.com/AlbrightAshleigh/Jenkins.git'


    stage 'Maven build'
    def mvn_version = 'Maven'
    withEnv( ["PATH+MAVEN=${tool mvn_version}/bin"] ) {
    sh 'mvn install'
    sh 'mvn -Dmaven.test.failure.ignore install'
    }


}