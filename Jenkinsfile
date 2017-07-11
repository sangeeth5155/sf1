node {
     def SFDC_USERNAME

    def HUB_ORG1 =env.HUB_ORG
    def SFDC_HOST1=env.SFDC_HOST
    def JWT_KEY_CRED_ID1=env.JWT_CRED_ID

    def CONNECTED_APP_CONSUMER_KEY1=env.CONNECTED_APP_CONSUMER_KEY
            println SFDC_HOST1
            println JWT_KEY_CRED_ID1
            println CONNECTED_APP_CONSUMER_KEY1
            println HUB_ORG1
			println env.HUB_ORG
   
    def toolbelt = tool 'SFDX CLI'
    stage('checkout SCM'){
    checkout scm
    }
}
