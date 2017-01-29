node{
    checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: '3c482a54-c880-496b-8325-f58976548456', url: 'https://github.com/sreenadhkumar/java_maven.git']]])
    def mvnHome = tool 'Maven-3.3.9'
    env.PATH = "${mvnHome}/bin:${env.PATH}"
    rtMaven.tool = "Maven-3.3.9"
    def buildInfo = rtMaven.run pom: 'maven-example/pom.xml', goals: 'clean install'

}
