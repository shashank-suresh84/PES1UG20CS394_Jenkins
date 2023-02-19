pipeline{
  agent any
  stages {
    stage('Build'){
      steps{
        sh 'g++ hello.cpp'
        build job : 'PES1UG20CS394-1'
        echo 'built'
      }
    }
    stage('Test'){
      steps{
        sh './a.out'
        echo 'Tested'
      }
    }
  }
  post{
    failure{
      echo 'Failed'
    }
  }
}
