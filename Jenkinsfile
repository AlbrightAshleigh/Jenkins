node{
    stage 'Checkout'
    git url: 'https://github.com/AlbrightAshleigh/Jenkins.git'


    stage 'Maven build'
    def mvn_version = 'Maven'
    withEnv( ["PATH+MAVEN=${tool mvn_version}/bin"] ) {
    sh 'mvn install'
    }

    stage 'User Acceptance Test'
    def response= input message: 'Is this build good to go?',
        parameters: [choice(choices: 'Yes\nNo',
        description: '', name: 'Pass')]

//     if(response=='Yes') {
//       node{
//       stage 'Deploy'
//       def mvn_version1 = 'Maven'
//       withEnv( ["PATH+MAVEN=${tool mvn_version1}/bin"] ) {
//       sh 'mvn install'
//           }
//       }
//
//     }


}