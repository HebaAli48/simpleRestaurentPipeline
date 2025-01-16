pipeline {
    agent any
  
    stages {
        // stage('Checkout') {
        //     steps {
        //         // Checkout the code from Git repository
        //         git 'https://github.com/HebaAli48/simpleRestaurentPipeline.git'
        //     }
        // }

        stage('Install Dependencies') {
            steps {
                // Install any dependencies (if needed, such as npm packages or tools)
                script {
                    echo 'No dependencies for HTML/CSS/JS app.'
                }
            }
        }

        stage('Linting') {
            steps {
                // Run linting to check for code quality issues (if you have ESLint or similar tools)
                script {
                    echo 'Running linting to check for code quality issues.'
                    // Example: sh 'eslint src/**/*.js'
                }
            }
        }

        stage('Build') {
            steps {
                // If you have build steps, like minification or bundling, you can do it here
                script {
                    echo 'Building the app (minification, bundling, etc.)'
                    // Example: sh 'npm run build' (if using a bundler like Webpack)
                }
            }
        }

        stage('Test') {
            steps {
                // Run any tests for the app (if you have unit or integration tests)
                script {
                    echo 'Running tests (if any are set up)'
                    // Example: sh 'npm test'
                }
            }
        }

        stage('Deploy') {
            steps {
                // Deploy the app to the target environment (this depends on how you're deploying it)
                script {
                    echo 'Deploying the app to production/staging environment.'
                    // Example: Copy files to server or deploy to hosting platform
                    // Example: sh 'scp -r * user@server:/var/www/html'
                }
            }
        }

        stage('Clean Up') {
            steps {
                // Clean up temporary files (optional)
                script {
                    echo 'Cleaning up temporary files.'
                    // Example: sh 'rm -rf dist'
                }
            }
        }
    }

    post {
        success {
            echo 'Build and Deployment Successful!'
        }
        failure {
            echo 'Something went wrong. Please check the build logs!'
        }
    }
}
