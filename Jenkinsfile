// version 1
// pipeline {
//     agent {
//         docker {
//             image 'node:6-alpine'
//             args '-p 3000:3000 -p 5000:5000' 
//         }
//     }
//     environment {
//         // operate it in docker root level
//         HOME = '.'
//         CI = 'true'
//     }
//     stages {
//         stage('Build') {
//             steps {
//                 sh 'npm install'
//             }
//         }

//         stage('Test') {
//             steps {
//                 sh './jenkins/scripts/test.sh'
//             }
//         }

//         stage('Deliver for development') {
//             when {
//                 branch 'development'
//             }
//             steps {
//                 sh './jenkins/scripts/deliver-for-development.sh'
//                 input message: 'Finished using the web site? (Click "Proceed" to continue)'
//                 sh './jenkins/scripts/kill.sh'
//             }
//         }
        
//         stage('Deploy for production') {
//             when {
//                 branch 'production'
//             }
//             steps {
//                 sh './jenkins/scripts/deploy-for-production.sh'
//                 input message: 'Finished using the web site? (Click "Proceed" to continue)'
//                 sh './jenkins/scripts/kill.sh'
//             }
//         }

//     }
// }


// version 2
// pipeline {
//     agent any
//     environment {
//         RELEASE='20.04'
//     }
//     stages {
//         stage('Build') {
//             agent any
//             // 有scope的environment variable
//             environment {
//                 LOG_LEVEL='INFO'
//             }
//             steps {
//                 echo "Building release ${RELEASE} with log level ${LOG_LEVEL}..."
//             }
//         }
//         stage('Test') {
//             steps {
//                 // 此环境变量无法被访问
//                 echo "Testing. I can see release ${RELEASE}, but not log level ${LOG_LEVEL}"
//             }
//         }
//     }
// }

// version 3
