pipeline{
 agent any
    stages {
        stage('step 1 : Clone code from Git') {
            steps {
                echo "GitHub clone step"
                git branch: "aymen",
                url: "https://github.com/aymenESP/achatDEVOPS.git"
            }
        }
        stage('step 2 : Compile & test Maven') {
            steps {
                sh 'mvn clean compile -DskipTests'
                sh 'mvn test'
            }
        }
 }
    
}
