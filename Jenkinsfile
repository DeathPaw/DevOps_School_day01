pipeline {
    agent any
    triggers { pollSCM('H */4 * * 1-3') }
    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                sh 'docker build -t 285484/weather-app .'
            }
        }
//         stage('Deploy') {
//             steps {
//                 echo 'Deploying to docker hub....'
//                 sh 'docker push 285484/weather-app'
//             }
//         }
//         stage('Running') {
//             steps {
//                 echo 'Starting service....'
//                 sh 'docker run --rm --name weather-app -p 8080:8080 --env API_KEY_WEATHER=<your_key> -d weather-app'
//             }
//         }
    }
}