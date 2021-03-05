pipeline {
    agent { label 'master' }
    
    parameters {
       extendedChoice(description: '', multiSelectDelimiter: ',', name: 'Masspay-Test-Suite', quoteValue: true, saveJSONParameterToFile: false, type: 'PT_CHECKBOX', value: 'Masspay-DEV,Masspay-SIT,Masspay-QA,Masspay-PROD', visibleItemCount: 4)    
      }
    stages {	
	    
	    
               stage('build') {
            steps {
                cleanWs()
        
              script {
	def mp ="${params.'Masspay-Test-Suite'}"
        String[] str;
      str = mp.split(','); 
	      for(int i = 0; i < str.length ; i++)
               println (str[i]);	      
		      
        }  
	    }           
        }
		
		}
		
		}
