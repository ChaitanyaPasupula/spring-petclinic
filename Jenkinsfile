node{
    stage("SCM"){
        git 'https://github.com/ChaitanyaPasupula/game-of-life.git'
    }
    stage("Build"){
        sh 'mvn package'
    }
    stage("Results"){
        archiveArtifacts 'gameoflife-web/target/gameoflife.war'
        junit 'gameoflife-web/target/surefire-reports/*.xml'
    }
}