#### Parser Content
```Java
{
Name = amazon-awsguardduty-json-database-login-success-rdssuccessfullogin
  Conditions = [ """"serviceName":"guardduty"""", """"type":"CredentialAccess:RDS/AnomalousBehavior.SuccessfulLogin"""" ]
  ParserVersion = "v1.0.0"
  Fields = ${AwsGuardDutyParserTemplates.json-aws-guardduty-security-alert-template.Fields} [
    """"userName":"(({aws_email_address}({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|({aws_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))"""",
    """exa_regex="userName":"(({aws_email_address}({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|({aws_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))"""
  ]

json-aws-guardduty-security-alert-template = {
    Vendor = Amazon
    Product = AWS GuardDuty
    ExtractionType = json
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
    Fields = [
      """"updatedAt":\s*"({time}\d{4}-\d{2}-\d{2}T(\d{2}:){2}\d{2}\.\d+Z)"""",
      """"ipAddressV4":\s*"({src_ip}(\d{1,3}\.){3}\d{1,3})"""",
      """"title":"(({event_name}[^"]+?(instance|bucket|database))(\s[^"\s]+?)?|({=event_name}[^"]+?))",""",
      """"type":"({alert_type}[^"]+):({alert_name}[^"]+)",""",
      """"severity":\s*({alert_severity}[\d.]+),""",
      """"region":\s*"({region}[^"]+?)",""",
      """"description":\s*"({additional_info}[^"]+?)"""",
      """"accountId":\s*"({account_id}[^"]+?)","""
      """domain":"({domain}[^"]+)"""",
      """resource":[^}]+principalId":\s*"([^},]+?(:({aws_email_address}({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))))?)"""",
      """resource":[^}]+"userName":\s*"({aws_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))"[^\}]+?"userType":\s*"(?!AssumedRole)[^"]+"""",
      """resource":[^}]+"userType":\s*"(?!AssumedRole)[^"]+"[^\}]+?"userName":\s*"({aws_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""",
      """resource":[^}]+"userType":\s*"({user_type}[^},]+?)"""",
      """key":"PrincipalId","value":"([^:]+:)?({aws_email_address}({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)))"""",
      """"resourceType":\s*"({resource_type}[^"]+)"""",
      """s3BucketDetails:\s*\[\{Arn:\s*({object}[^,]+),Name:""",
      """"instanceId":"({instance_id}[^"]+)"""",
      """"city":\{"cityName":"((?i)UNKNOWN|({location_city}[^"]+))""""
      """\ssuser=(|Anonymous|({aws_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\s+(\w+=|$)""",
      """"service".*?"action".*?"networkConnectionAction.*?({result}"blocked":"*(false|true))"""
      """"accountId":"({aws_account}\d+)"""
      """\srequestClientApplication=({app}\S+)""",
      """\sdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
      """"privateIpAddress":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
      """"resource":[^=]+?privateIpAddress":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
      """"service".*?"action".*?"portProbeAction".*?"portProbeDetails".*?"localPortDetails".*?"port":"*({dest_port}\d+)"*""",
      """"service".*?"action".*?"networkConnectionAction".*?"localPortDetails".*?"port":({dest_port}\d+)"""
      """"id":"({alert_id}[^"]+?)"""",
      """"userName":"(({aws_email_address}({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|({aws_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))"[^\}]+?"userType":\s*"(?!AssumedRole)[^"]+""""
      """"userType":\s*"(?!AssumedRole)[^"]+"[^\}]+?"userName":"(({aws_email_address}({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|({aws_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))""""
      """"key":"ProductOwner","value":"({aws_email_address}({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)))""""
      """"accessKeyId":"({key_id}[^"]+?)""""
      """"+iamInstanceProfile.+?arn\\?":\s*\\?"({instance_profile_arn}[^"]+?)\\?"""",
      """"tags":\[({tags}.+"\})\]\}""",
      """exa_json_path=$.updatedAt,exa_field_name=time"""
      """exa_json_path=$.awsRegion,exa_field_name=region"""
      """exa_regex="ipAddressV4":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
      """exa_json_path=$.resource.resourceType,exa_field_name=resource_type"""
      """exa_json_path=$.description,exa_field_name=additional_info"""
      """exa_json_path=$.accountId,exa_field_name=account_id""",
      """exa_json_path=$.resource.accessKeyDetails.userName,exa_field_name=user""",
      """exa_json_path=$.severity,exa_field_name=alert_severity""",
      """exa_json_path=$.region,exa_field_name=region""",
      """exa_json_path=$.resource.accessKeyDetails.userType,exa_field_name=user_type"""
      """exa_json_path=$.readOnly,exa_field_name=readonly""",
      """exa_regex="userName":"(({aws_email_address}({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|({aws_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))"[^\}]+?"userType":\s*"(?!AssumedRole)[^"]+"""",
      """exa_regex="userType":\s*"(?!AssumedRole)[^"]+"[^\}]+?"userName":"(({aws_email_address}({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|({aws_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))"""",
      """exa_json_path=$.eventName,exa_field_name=event_name""",
      """exa_json_path=$.destinationServiceName,exa_field_name=app""",
      """exa_json_path=$.userAgent,exa_field_name=user_agent""",
      """exa_json_path=$.serviceEventDetails.account_id,exa_field_name=account_id""",
      """exa_json_path=$.eventTime,exa_field_name=time""",
      """exa_json_path=$.eventSource,exa_field_name=src_host""",
      """exa_json_path=$.eventID,exa_field_name=alert_id""",
      """exa_json_path=$.eventCategory,exa_field_name=event_category"""
      """exa_regex="sourceIPAddress":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
      """exa_regex="resource":[^=]+?privateIpAddress":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""""
      """exa_regex="title":"(({event_name}[^"]+?(instance|bucket|database))(\s[^"\s]+?)?|({=event_name}[^"]+?))","""
      """exa_regex="type":"({alert_type}[^"]+):({alert_name}[^"]+)","""
      """exa_regex="city":\{"cityName":"((?i)UNKNOWN|({location_city}[^"]+))""""
      """exa_json_path=$.service.action.kubernetesApiCallAction.remoteIpDetails.city.cityName,exa_field_name=location_city"""
      """exa_json_path=$.resource.instanceDetails.instanceId,exa_field_name=instance_id"""
      """exa_regex="accessKeyId":"({key_id}[^"]+?)""""
      """dhost=({dest_host}[\w\-.]+)"""
      """exa_json_path=$.resource.tags,exa_field_name=tags"""
    
}
```