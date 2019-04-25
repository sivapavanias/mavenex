pipeline {
    agent any
	tools {
	 maven 'maven_3_5_0'
	}
	environment {
		def maven = tool name: 'maven_3_5_0', type: 'maven'
		def JAVA_HOME = tool name: 'jdk1.8.0_191', type: 'jdk'
	}

    stages {
        stage ('Compile Stage') {

            steps {
                withMaven(maven : 'maven_3_5_0') {
			sh "hello world"
			

                sh  'mvn clean compile'
			echo 'compiling'
                }
            }
        }

        stage ('Testing Stage') {

            steps {
                withMaven(maven : 'maven_3_5_0') {
                   sh 'mvn test'
			echo 'testing.......'
	           }
            }
        }
    }
}
