node('master') {
    // some block
	checkout scm
	stage('Build') {
    // some block
    withMaven(maven: 'M3') {
    // some block
      if(isUnix()){
        sh label: '', script: 'mvn -Dmaven.test.failure.ignore clean package'
      }else{
        bat 'mvn -Dmaven.test.failure.ignore clean package'
      }
    	
	}
	}
   stage('Results') {
    // some block
    junit '**/target/surfire-reports/TEST-*.xml'
    archive 'target/*.jar'
	}
}
