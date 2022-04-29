pipeline {
agent any
stages {
stage ('Compile Stage') {
steps {
withMaven(maven : 'apache-maven-3.6.1') {
sh 'mvn clean'
}
}
}
stage ('Testing Stage') {
steps {
withMaven(maven : 'apache-maven-3.6.1') {
bat'mvn test'
}
}
}
stage ('Install Stage') {
steps {
withMaven(maven : 'apache-maven-3.6.1') {
bat'mvn install'
}
}
}
}
}

