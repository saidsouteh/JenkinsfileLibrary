node("master"){
       stage ('SCM Checkout') { 
         git branch: '${BRANCH}', url: ' https://github.com/saidsouteh/${COLLECTION}.git'
                       }

        stage ('MOLECULE DEPENDENCY') {
        sh 'export PATH=$PATH:/usr/local/bin ; ls roles/ | xargs -L 1 bash -c \'cd "roles/$0" && molecule dependency\''   
          }
        stage ('MOLECULE LINT') {
        sh 'export PATH=$PATH:/usr/local/bin ; ls roles/ | xargs -L 1 bash -c \'cd "roles/$0" && molecule lint\''   
          }
        stage ('MOLECULE CREATE') {
        sh 'export PATH=$PATH:/usr/local/bin ; ls roles/ | xargs -L 1 bash -c \'cd "roles/$0" && molecule create\''   
          }
        stage ('MOLECULE CONVERGE') {
        sh 'export PATH=$PATH:/usr/local/bin ; ls roles/ | xargs -L 1 bash -c \'cd "roles/$0" && molecule converge\''   
          }
         stage ('MOLECULE idempotence') {
        sh 'export PATH=$PATH:/usr/local/bin ; ls roles/ | xargs -L 1 bash -c \'cd "roles/$0" && molecule idempotence\''   
          }
         stage ('MOLECULE verify') {
        sh 'export PATH=$PATH:/usr/local/bin ; ls roles/ | xargs -L 1 bash -c \'cd "roles/$0" && molecule verify\''   
          }
        stage ('MOLECULE destroy') {
        sh 'export PATH=$PATH:/usr/local/bin ; ls roles/ | xargs -L 1 bash -c \'cd "roles/$0" && molecule destroy\''   
          }
    
    
    
} 
