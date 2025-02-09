pipeline{
  agent any
  stages{
    stage("Installing the dependencies"){
      // this stage happens first then parallel execution starts,
      steps{
        echo "Installing the dependencies"
      }
    }
    stage("Parallel execution phase"){
      parallel{
        stage('Build windows'){
          steps{
            echo "Executing Task 1"
            script{
              sleep(4) 
              echo "Task 1 completed :Building for Windows "}
          }
        }
        stage('Build Linux'){
          steps{
            echo "Executing Task 2 : Building for Linux"
            script{
              sleep(2)
              echo "Task 2 completed "}
          }
        }
        stage('Build Macos'){
          steps{
            echo "Executing Task 3 : Building for MAC"
            script{
              sleep(2) 
              echo "Task 3 completed "}
          }
        }
      }
    }
  }
}
