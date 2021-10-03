node {
    stage ('Preperation'){
        git branch: 'dvir', credentialsId: 'GitHub', url: 'https://github.com/dvirblu/jenkins-pipeline-exercise.git'

    }
    stage ('Build'){
        sh'pwd'
        sh'./gradlew clean test jar'
    }
    stage ('Result'){
        junit '**/build/test-results/test/TEST-*.xml'
        archiveArtifacts 'build/libs/*'
    }
}