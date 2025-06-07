pipeline{
agent any

tools{
maven 'Maven'
jdk 'JDK'
}

stages{

stage('checkout'){
steps{
git branch:'master',url:'https://github.com/Sach791/maven7.git'

}
}

stage('build'){
steps{
sh 'mvn build clean package'
}
}

stage('test'){
steps{
sh 'mvn test'
}
}

stage('Run Application'){
steps{
sh 'java -jar target/maven7-1.0-SNAPSHOT.jar'
}
}
}

post{
success{
echo 'build and deployment successfull'
}
failure{
echo 'deployed failed!'
}
}
}

