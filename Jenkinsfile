pipeline{
 agent any
    stages {
        stage('Step 1 : Clone code from Git') {
            steps {
                echo "GitHub clone step"
                git branch: "aymen",
                url: "https://github.com/aymenESP/achatDEVOPS.git"
            }
        }
        stage('Step 2 : Compile & test Maven') {
            steps {
                sh 'mvn clean compile -DskipTests'
                sh 'mvn test'
            }
        }
             stage('Step 3 : Run SonarQube') {
            steps {
                sh   "mvn sonar:sonar -Dsonar.projectKey=devopsproject -Dsonar.host.url=http://192.168.1.124:9090 -Dsonar.login=91c548fabf0c6bdab48d8f24ad26aa6a74b10d2f"
            }
        }
 }
    
}
