node{
     stage('SCM Checkout'){
	git url: 'https://github.com/Ram423/flyway.git'
	}
     stage('Maven clean'){
	def mvnHome = tool name: 'MAVEN-3.6', type: 'maven'
	def mvnCMD = "${mvnHome}/bin/mvn"
	sh label: '', script: "${mvnCMD} clean flyway:migrate -Dflyway.configFile=flyway.properties"
	}
} 