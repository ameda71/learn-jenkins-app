pipeline{
    agent any
    stages{
        stage("Build"){
            agent {
                docker{
                    image 'node:20-alpine'
                    
                }
            }
            steps{
              sh ''' 
              chown -R 777:777 "/.npm"
              ls -la
               node --version
               npm --version
               npm ci
               npm run build
              ls -la
              '''
        }
    }
}
}
