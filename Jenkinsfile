pipeline{
    agent any
    tools{
        jdk: 'jdk_11.0.27'
    }
    environment {
      NAME = "Jenkins"
      MACHINE = "Linux"
      JAVA_OPTS="-Xms128m -Xmx512m" 
    }
    stages{
        stage('Compiling'){
            environment{
                AUTHOR='Leandro B Silva'
            }
            steps{
                echo "Compilando o código"
                sh 'javac Param.java'
                sh 'The Author is ${AUTHOR}'
            }
        }
        stage('Execute'){
            steps{
                echo "Execute the program with a parameter "
                sh 'java Param ${NAME}'
            }
        }
        stage('Display the machine name'){
            steps{
               echo "And here I display name of the machine"
               sh 'javac Maquina.java'
               sh 'java Maquina ${MACHINE}'
            }
        }
    }
}