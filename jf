node {
 // stage1: clone the code
  stage('SCM') {
    git 'https://github.com/wakaleo/game-of-life.git'
} 
// stage2: build the code
stage('build code') {
    sh label: '', script: 'mvn package'
} 
//stage3: archive artifactory
stage('archive') {
   archive 'gameoflife-web/target/gameoflife.war'
}
//Publish Junit results
stage('Junit'){
   junit 'gameoflife-web/target/surefire-reports/*.xml' 
}
}
