pipeline{

agent any

tools{
maven 'mymaven'
}

parameters{
 choice(name: "ENV",choices: ["","Dev","QA"])
}

stages{
   stage('Build on Dev Env')
   {
     when{   // keyword for if  
      expression{params.ENV == "Dev"}  // condition to be satisfied 
     }
     steps{
     git 'https://github.com/Sonal0409/DevOpsCodeDemo.git'
     bat 'mvn compile'
     }
   }
   stage('Build on QA Env')
   {
   when{   // keyword for if  
    expression{params.ENV == "QA"}  // condition to be satisfied 
   }
   steps{
   git 'https://github.com/Sonal0409/DevOpsCodeDemo.git'
   bat 'mvn test'
   }
   
   }

}
}
