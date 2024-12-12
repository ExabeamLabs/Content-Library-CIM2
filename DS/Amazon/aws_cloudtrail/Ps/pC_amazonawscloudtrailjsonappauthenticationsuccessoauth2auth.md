#### Parser Content
```Java
{
Name = amazon-awscloudtrail-json-app-authentication-success-oauth2auth
  ParserVersion = v1.0.0
  Conditions = [ """"eventName":""", """"OAuth2_Authorize_GET"""", """"eventType":""", """"AwsServiceEvent"""" ]
  Fields = ${DLAwsParserTemplates.aws-cloudtrail-json-1.Fields}[
    """"status":({result_code}\d+)""",
    """"serviceAccountId":"({service_id}[^"]+)"""",
    """"response_type":\[?"({response_type}[^"]+)"\]?""",
    """"client_id":\[?"({client_id}[^"]+)"\]?""",
    """"userPoolDomain":"({domain}[^"]+)"""",
    """"userPoolId":"({user_id}[^"]+)""""
  ]

aws-cloudtrail-json-1 = {
  Vendor = Amazon
  Product = AWS CloudTrail
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  ExtractionType = json
  Fields = [
      """exa_json_path=$.eventTime,exa_field_name=time"""
      """exa_json_path=$.destinationServiceName,exa_field_name=app"""
      """exa_json_path=$.awsAccountId,exa_field_name=account_id"""
      """exa_json_path=$.userIdentity.accountId,exa_field_name=account_id"""
      """exa_json_path=$.sourceIPAddress,exa_regex=^(\s*|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)$"""
      """exa_json_path=$.eventSource,exa_field_name=src_host"""
      """exa_json_path=$.userAgent,exa_field_name=user_agent"""
      """exa_json_path=$.eventType,exa_field_name=event_category"""
      """exa_json_path=$.eventName,exa_field_name=event_name"""
      """exa_regex="userIdentity"\s*:\s*\{.*?(("type"\s*:\s*"Role")[^\}]*?"userName"\s*:\s*"({role}[^"]+)|"userName"\s*:\s*"({aws_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))""""
      """exa_regex="userIdentity"\s*:\s*\{.*?("type":\s*"AssumedRole").*?"principalId"\s*:\s*"([^},]+?(:({aws_email_address}({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))))?)""""
      """exa_regex="userIdentity"\s*:\s*\{.*?"principalId"\s*:\s*"([^},]+?(:({aws_email_address}({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))))?)".*?("type":\s*"AssumedRole")"""
      """exa_json_path=$..accessKeyId,exa_field_name=key_id,exa_match_expr=!InList(toLower($..accessKeyId), "")"""
      """exa_json_path=$.serviceAccountId,exa_field_name=service_id"""
      """exa_json_path=$.errorCode,exa_field_name=failure_code"""
      """exa_json_path=$.userPoolDomain,exa_field_name=domain"""
      """exa_json_path=$.userPoolId,exa_field_name=user_id"""
      """exa_json_path=$.status,exa_field_name=result_code"""
      """exa_json_path=$.recipientAccountId,exa_field_name=aws_account"""
    """"eventTime":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)"""",
	  """"destinationServiceName":"({app}[^"]+)"""",
	  """"awsAccountId":"({account_id}[^"]+)"""",
	  """"userIdentity":.*?"accountId":"({account_id}[^"]+)"""",
	  """"sourceIPAddress":"(\s*|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)"""",
	  """"eventSource":"(\s*|({src_host}[^"]+))"""",
	  """"userAgent":"(\s*|({user_agent}[^"]+))"""",
	  """"eventType":"({event_category}[^"]+)"""",
	  """"eventName":"({event_name}[^"]+)"""",
	  """"userIdentity"\s*:\s*\{.*?(("type"\s*:\s*"Role")[^\}]*?"userName"\s*:\s*"({role}[^"]+)|"userName"\s*:\s*"({aws_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))"""",
    """"userIdentity"\s*:\s*\{.*?("type":\s*"AssumedRole").*?"principalId"\s*:\s*"([^},]+?(:({aws_email_address}({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))))?)"""",
    """"userIdentity"\s*:\s*\{.*?"principalId"\s*:\s*"([^},]+?(:({aws_email_address}({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))))?)".*?("type":\s*"AssumedRole")""",
	  """"accessKeyId":"({key_id}[^"]+?)""""
  
}
```