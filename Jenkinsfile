pipeline{
  agent any
    tools{
        maven "MAVEN_HOME"
    } 
  
  stages
  {
    stage("Stage-1 check My code pl")
    {
      steps
      {
        git branch:'main', changelog:false,poll:false,url:"https://github.com/PrateekJain3185092/Jenkins_Assignment.git"
      }
    }
      stage("Stage-2 compile the given code pls")
      {
        steps
        {
          bat "mvn compile"
        }
      }
        stage ("Test my code pl")
        {
          steps{
            bat "mvn test"
          }
        }
          stage ("Check my package")
          {
          steps
          {
            bat "mvn package"
          }
        }
    }
}
