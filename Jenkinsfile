pipeline {  
//Donde se va a ejecutar el Pipeline  
  agent {
    label 'Slave_Induccion'
  }
  
  //Opciones específicas de Pipeline dentro del Pipeline  
  options {
    //Mantener artefactos y salida de consola para el # específico de ejecucionesrecientes del Pipeline.
    buildDiscarder(logRotator(numToKeepStr: '3'))
    //No permitir ejecuciones concurrentes de Pipeline
      disableConcurrentBuilds()  
  }
  
    //Una sección que define las herramientas para “autoinstalar” y poner en la PATH  
  tools {    
    jdk 'JDK8_Centos' //Preinstalada en la Configuración del Master    
    gradle 'Gradle4.5_Centos' //Preinstalada en la Configuración del Master  
  }
  
    //Aquí comienzan los “items” del Pipeline  
  stages{
    stage('Checkout') {
      steps{
        echo "------------>Checkout<------------"      
      }
    }
    
    stage('Unit Tests') {      
      steps{        
        echo "------------>Unit Tests<------------"      
      }    
    }
    
    stage('Integration Tests') {      steps {        echo "------------>Integration Tests<------------"      }    }
