#### Parser Content
```Java
{
Name = amazon-awscloudtrail-json-configuration-modify-success-updatestack
  Conditions = [ """AwsApiCall""", """"eventName":""", """"UpdateStack"""" ]
  Fields = ${AwsParserTemplates.aws-cloudtrail-json.Fields}[
    """"+requestParameters":\{("[^,]+,)*"stackName\\?":\s*\\?"({object}[^"]+?)\\?"""",
  ]
  ParserVersion = v1.0.0

aws-cloudtrail-json = {
    Vendor = Amazon
    Product = AWS CloudTrail
    ExtractionType = json
    TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ","yyyy-MM-dd'T'HH:mm:ssZ"]
    Fields = [
      """"instanceId\\?":\\?"({instance_id}[^"]+?)\\?""""
      """"userIdentity":\{("[^,]+,)*"type"\\?:\s*\\?"({user_type}[^"]+?)\\?"""",
      """"userIdentity":\{("[^,]+,)*"arn"\\?:\s*\\?"({user_arn}[^"]+?)\\?"""",
      """"userIdentity":\{("[^,]+,)*"accountId\\?"+\s*:\s*\\?"+?({aws_account}[^"]+?)\\?"+\s*[,\]\}]""",
      """"userIdentity":\{("[^,]+,)*"principalId\\?"+\s*:\s*\\?"+?({principal_id}[^"]+?)\\?"+\s*[,\]\}]""",
      """"userIdentity":\{("[^,]+,)*"attributes":\{("[^,]+,)*"mfaAuthenticated"\\?:\s*\\?"({mfa}[^"]+?)\\?"""",
      """"assumedRoleUser":\{("[^,]+,)*"arn"\s*:\s*"({role_arn}[^"]+)\\?""""
      # """"eventTime"+\s*:\s*"+?(|({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)Z?)"+\s*[,\]\}]""",
      """"TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d\d\d\d\dZ)"""",
      """"eventTime"+\s*:\s*"+?(|({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ?))"+\s*[,\]\}]""",
      """"eventSource"+\s*:\s*"+?(|({service_name}[^"]+))"+\s*[,\]\}]""",
      """"eventName"+\s*:\s*"+?(|({operation}[^"]+))"+\s*[,\]\}]""",
      """"awsRegion"\s*:\s*"({region}[^"]+)"""",
      """"tlsDetails":.*?clientProvidedHostHeader":"({src_host}[\w\-\.]+)"""
      """"sourceIPAddress"+\s*:\s*"+?(?:({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?|({src_host}[\w\-.]+))"+\s*[,\]\}]""",
      """"userAgent"\s*:\s*"\[?(|({user_agent}[^"]+?))\]?"""",
      """"eventID\\?"+:\\?"+({event_code}[^"\\]+)\\?"""",
      """"eventType"+\s*:\s*"+?(|({event_category}[^"]+))"+\s*[,\]\}]""",
      """"errorCode"\s*:\s*"({result}[^"]+)"""",
      """"errorMessage"\s*:\s*"({failure_reason}[^"]+)"""",
      """"readOnly"\s*:\s*({readonly}[^",\}]+)("|,|\}\s*$)""",
      """"vpcEndpointId":"({vpc}[^"]+)""",
      """"+requestParameters":\{("[^,]+,)*"roleSessionName\\?":\s*\\?"({session_name}[^"]+?)\\?"""",
      """"+responseElements":\{"assumedRoleUser":\{("[^,]+,)*"assumedRoleId\\?":\s*\\?"({role_id}[^"]+?)\\?"""",
      """"accessKeyId":"({key_id}[^"]+?)"""",
      #AWS CloudTrail user regexes
      """\Wsuser=[^=]*?(({email_address}[^@=\s\/:]+@[^=\.\s\/:]+\.[^\s=\/:]+?)|({user}[\w\.\-]{1,40}\$?)(@[^=]+?)?)(\s+\w+=|\s*$)""",
      """\\?"type\\?":\\?"IAMUser\\?"[^\}]+?"userName\\?":\s*\\?"(({email_address}[^"@]+@[^"\.]+\.[^"]+)|({user}[\w\.\-]{1,40}\$?)(@({domain}[^@"]+))?)\\?"""",
      """"userIdentity\\?":.+?"arn\\?":\s*\\?"arn:aws:sts::\d+:assumed-role\/([^\/"]+\/)(AssumeRoleSession|((?![\w\-\.]{30,})(({email_address}[^"@]+@[^"\.]+\.[^"]+)|({user}[\w\.\-]{1,40}\$?)(@({domain}[^@"]+))?)))\\?"""",
      """"sourceIdentity\\?":\s*\\?"(({email_address}[^"@]+@[^"\.]+\.[^"]+)|({user}[\w\.\-]{1,40}\$?)(@({domain}[^@"]+))?)\\?"""",
      """"userIdentity\\?":.+?"AssumedRole\\?".+?"principalId\\?":\s*\\?"[A-Z\d]{1,25}:({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))\\?"\s*[,\]\}]""",
      """"userIdentity\\?":.+?"AssumedRole\\?".+?"sessionIssuer\\?":\s*\{[^\}]+?"IAMUser\\?"[^\}]+?"userName\\?":\s*\\?"(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-]{1,40}\$?)(@({domain}[^@"]+))?)\\?"""",
      """"userIdentity\\?":.+?"IAMUser\\?".+?"userName\\?":\s*\\?"(({email_address}[^"@]+@[^"\.]+\.[^"]+)|({user}[\w\.\-]{1,40}\$?)(@({domain}[^@"]+))?)\\?"""",
      """"userIdentity\\?":\s*\{.*?"type\\?":\s*\\?"({user}Root)\\?""""
      """exa_json_path=$.userIdentity.type,exa_field_name=user_type""",
      """exa_json_path=$.userIdentity.arn,exa_field_name=user_arn""",
      """exa_json_path=$.userIdentity.accountId,exa_field_name=aws_account""",
      """exa_json_path=$.userIdentity.principalId,exa_field_name=principal_id""",
      """exa_json_path=$.userIdentity..attributes.mfaAuthenticated,exa_field_name=mfa""",
      """exa_json_path=$.TimeGenerated,exa_field_name=time""",
      """exa_json_path=$.eventTime,exa_field_name=time""",
      """exa_json_path=$.eventSource,exa_field_name=service_name""",
      """exa_json_path=$.eventName,exa_field_name=operation""",
      """exa_json_path=$.awsRegion,exa_field_name=region""",
      """exa_json_path=$.tlsDetails.clientProvidedHostHeader,exa_field_name=src_host""",
      """exa_json_path=$.sourceIPAddress,exa_regex=(?:({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?|({src_host}[\w\-.]+))$""",
      """exa_json_path=$.userAgent,exa_regex=\[?({user_agent}.*?)\]?$""",
      """exa_json_path=$.eventType,exa_field_name=event_category""",
      """exa_json_path=$.eventID,exa_field_name=event_code""",
      """exa_json_path=$.errorCode,exa_field_name=result""",
      """exa_json_path=$.errorMessage,exa_field_name=failure_reason""",
      """exa_json_path=$.readOnly,exa_field_name=readonly""",
      """exa_json_path=$.vpcEndpointId,exa_field_name=vpc""",
      #"""exa_json_path=$.userIdentity.userName,exa_regex=(({email_address}[^"@]+@[^"\.]+\.[^"]+)|({user}[\w\.\-]{1,40}\$?)(@({domain}[^@"]+))?)\\?,exa_match_expr=Contains(toLower($.userIdentity.type),"iamuser")""",
      """exa_json_path=$.userIdentity,exa_regex="type\\?":\\?"IAMUser\\?"[^\}]+?"userName\\?":\s*\\?"(({email_address}[^"@]+@[^"\.]+\.[^"]+)|({user}[\w\.\-]{1,40}\$?)(@({domain}[^@"]+))?)\\?"""",
      """exa_json_path=$.userIdentity.arn,exa_regex=arn:aws:sts::\d+:assumed-role\/([^\/"]+\/)(AssumeRoleSession|((?![\w\-\.]{30,})(({email_address}[^"@]+@[^"\.]+\.[^"]+)|({user}[\w\.\-]{1,40}\$?)(@({domain}[^@"]+))?)))\\?""",
      """exa_json_path=$.userIdentity.type,exa_regex=({user}Root)""",
      """exa_json_path=$.requestParameters.bucketName,exa_field_name=bucket_name""",
      """exa_json_path=$.requestParameters.Host,exa_field_name=bucket_host""",
      """exa_json_path=$.resources..ARN,exa_field_name=bucket_arn"""
      """exa_json_path=$.userIdentity.accessKeyId,exa_field_name=key_id"""
      """exa_json_path=$.requestParameters..InstanceId,exa_field_name=instance_id"""
      """exa_json_path=$.requestParameters..instanceId,exa_field_name=instance_id"""
      """exa_json_path=$.recipientAccountId,exa_field_name=aws_account"""
    
}
```