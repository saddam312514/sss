
pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                // Checkout your source code from the repository
                checkout scm
            }
        }
        // stage('Build') {
        //     steps {
        //         // Build your PHP application (e.g., run composer, compile assets, etc.)
        //         sh 'composer update && composer install'
        //         sh 'npm install'
        //         sh 'npm run production'
        //     }
        // }

stage('Build Tar File') {
            steps {
                // Create a tar file from your Laravel project files (replace with your tar command)
                sh 'tar -czf laravel-project.tar.gz *'
            }
        }
        stage('Archive Tar File') {
            steps {
                // Archive the tar file as an artifact
                archiveArtifacts artifacts: 'laravel-project.tar.gz', allowEmptyArchive: true
                //saddam
            }
        }
        
   // stage('Archive as ZIP') {
   //          steps {
   //              // Archive the Laravel project as a ZIP file using the full path
   //              archiveArtifacts allowEmptyArchive: true, artifacts: '/var/lib/jenkins/workspace/Package_install_Laravel/**/*'
   //          }
   //      }
         // stage('Deploy to Production'){
         //     steps{
         //         timeout(time:5, unit:'DAYS'){
         //             input message:'Approve PRODUCTION Deployment?'
         //         }
         //         build job: 'Deploy_Application_Prod_Env'
         //     }
         // }
    }
}
