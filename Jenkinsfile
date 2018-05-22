node{
    stage("SCM"){
        git 'https://github.com/ChaitanyaPasupula/spring-petclinic.git'
    }
    stage("Build"){
        sh 'mvn package'
    }
    stage("Results"){
        archiveArtifacts 'target/spring-petclinic-2.0.0.BUILD-SNAPSHOT.jar'
        junit 'target/surefire-reports/*.xml'
    }
}