#!groovy
import groovy.json.JsonSlurperClassic
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
	withCredentials([file(credentialsId: JWT_KEY_CRED_ID1, variable: 'jwt_key_file')]) {
        stage('Create Scratch Org') {

           echo "started"
            rc = bat returnStatus: true,script: "\"${toolbelt}/bin\bin\sfdx\" force:auth:jwt:grant --clientid ${CONNECTED_APP_CONSUMER_KEY1} --username ${HUB_ORG1} --jwtkeyfile ${jwt_key_file} --setdefaultdevhubusername"
            if (rc != 0) { error 'hub org authorization failed' }

	}
        }
}
