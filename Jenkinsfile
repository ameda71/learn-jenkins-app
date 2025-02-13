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
              sudo node --version
              sudo npm --version
              sudo npm ci
              sudo npm run build
              ls -la
              '''
        }
    }
}
}
