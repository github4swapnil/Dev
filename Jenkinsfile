pipeline {
   agent any

   stages {
      stage('Git Clone') {
         steps {             
             git url: 'https://github.com/github4swapnil/Dev.git'
         }
      }
      stage('Execute Stored Procedure')
      {
          steps{
           sh label: '', script: 
                '''for sql_file in *.sql 
                        do 
                           echo "${sql_file}" 
                           /opt/mssql-tools/bin/sqlcmd -S qacop.ccz8gy1ujvhp.us-east-2.rds.amazonaws.com,1433 -U swapniln -P swapnilqacop -i "${sql_file}"
                        done
                '''
               )
                  '''
          }
      }
   }
}
