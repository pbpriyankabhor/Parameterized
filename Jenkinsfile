pipeline {
    agent any
    parameters {
        string(name: 'maven_version', defaultValue: '3.9.6', description: 'pass the version of maven')
        string(name: 'terraform_version', defaultValue: '1.7.5', description: 'pass the version of terraform')
    }
    stages {
        stage('download maven') {
            steps {
		        sh 'cd /var/lib/jenkins/'
                sh 'sudo wget https://dlcdn.apache.org/maven/maven-3/$maven_version/binaries/apache-maven-$maven_version-bin.tar.gz'
            }
        }
        stage('download terraform') {
            steps {
	            sh 'cd /opt'
                sh 'sudo wget https://releases.hashicorp.com/terraform/$terraform_version/terraform_${terraform_version}_linux_amd64.zip'
            }
        }		
   }
}
