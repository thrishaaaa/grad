pipeline{
    agent any
    tools{
      gradle 'Gradle'
      jdk 'JDK' 
    }
    stages{
      stage('Checkout'){
        steps{
          git branch:'main' , url:'https://github.com/thrishaaaa/grad.git'
        }
      }
      stage('Build'){
        steps{
          sh '/opt/gradle/gradle-8.0.2/bin/gradle build'
        }
      }
      stage('Run Application'){
        steps{
          sh'gradle run'
        }
      }
    }
    
    post{
      success{
        echo 'Build gradle appliaction successfully'
      }
      failure{
       echo 'Build failed'
      }
    }
    
}
