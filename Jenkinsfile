pipeline {
  agent {
    docker {
      image 'maven:3.8.1-jdk-11-slim'
    }

  }
  stages {
    stage('build') {
      steps {
        echo 'Compile'
        sh 'mvn compile'
      }
    }

    stage('test') {
      steps {
        echo 'Test'
        sh 'mvn clean test'
      }
    }

    stage('package') {
      steps {
        echo 'Package'
        sh 'mvn package -DskipTests'
        archiveArtifacts 'target/*.war'
      }
    }

  }
  tools {
    maven 'Maven 3.6.3'
  }
}