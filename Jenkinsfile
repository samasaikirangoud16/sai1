node ('dev') {
    tool 'maven'
    stage('Git') { 
        git branch: 'main', url: 'https://github.com/samasaikirangoud16/sai1.git'
    }
    stage('Build') {
        sh 'mvn clean package'
        }
    stage('Deploy') {
        deploy adapters: [tomcat9(credentialsId: 'tomcat', path: '', url: 'http://3.110.54.148:8081/')], contextPath: 'kiran', war: '**/*.war'
    }
}
