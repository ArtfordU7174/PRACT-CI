pipeline{
     agent any
     tools {
        maven 'maven3'
        jdk 'oracleJDK8'
    }
    environment{
        SNAP_REPO = 'vpro-snapshots'
        NEXUS_USER = 'admin'
        NEXUS_PASS = 'nexus'
        RELEASE_REPO = 'vpro-release'
        CENTRAL_REPO = 'vpro-maven-central'
        NEXUS_IP = '172.31.9.202'
        NEXUS_PORT = '8081'
        NEXUS_GRP_REPO = 'vpro-maven-group'
        NEXUS_LOGIN = 'nexuslogin' 
    }
    stages{
        stage('BUILD'){
            steps{
                sh 'mvn -s settings.xml install -DskipTests'
            }
        }
    }

}
