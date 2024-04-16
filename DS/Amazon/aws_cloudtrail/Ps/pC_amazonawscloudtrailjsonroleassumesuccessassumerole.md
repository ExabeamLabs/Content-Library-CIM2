#### Parser Content
```Java
{
Name = amazon-awscloudtrail-json-role-assume-success-assumerole
  Vendor = Amazon
  Product = AWS CloudTrail
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ","yyyy-MM-dd'T'HH:mm:ssZ"]
  Conditions = [ """AwsApiCall""", """"eventName":""", """"AssumeRole"""" ]
  Fields = ${AwsParserTemplates.aws-cloudtrail-user-template.Fields}[
      """"TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)"""" 
      """"userIdentity":\{("[^,]+,)*"type"\\?:\s*\\?"({user_type}[^"]+?)\\?"""",
      """"userIdentity":\{("[^,]+,)*"arn"\\?:\s*\\?"({user_arn}[^"]+?)\\?"""",
      """"userIdentity":\{("[^,]+,)*"accountId\\?"+\s*:\s*\\?"+?({aws_account}[^"]+?)\\?"+\s*[,\]\}]""",
      """"userIdentity":\{("[^,]+,)*"principalId\\?"+\s*:\s*\\?"+?({principal_id}[^"]+?)\\?"+\s*[,\]\}]""",
      """"userIdentity":\{("[^,]+,)*"attributes":\{("[^,]+,)*"mfaAuthenticated"\\?:\s*\\?"({mfa}[^"]+?)\\?"""",
      """"assumedRoleUser":\{("[^,]+,)*"arn"\s*:\s*"({assumed_role_arn}[^"]+)\\?""""
      """"TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d\d\d\d\dZ)"""",
      """"eventTime"+\s*:\s*"+?(|({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ))"+\s*[,\]\}]""",
      """"eventSource"+\s*:\s*"+?(|({service_name}[^"]+))"+\s*[,\]\}]""",
      """"eventName"+\s*:\s*"+?(|({operation}[^"]+))"+\s*[,\]\}]""",
      """"awsRegion"\s*:\s*"({region}[^"]+)"""",
      """"tlsDetails":.*?clientProvidedHostHeader":"({src_host}[\w\-\.]+)"""
      """"sourceIPAddress"+\s*:\s*"+?(?:({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?|({src_host}[^"]+))"+\s*[,\]\}]""",
      """"userAgent"\s*:\s*"\[?(|({user_agent}[^"]+?))\]?"""",
      """"eventID\\?"+:\\?"+({event_code}[^"\\]+)\\?"""",
      """"eventType"+\s*:\s*"+?(|({event_category}[^"]+))"+\s*[,\]\}]""",
      """"errorCode"\s*:\s*"({result}[^"]+)"""",
      """"errorMessage"\s*:\s*"({failure_reason}[^"]+)"""",
      """"readOnly"\s*:\s*({readonly}[^",\}]+)("|,|\}\s*$)""",
      """"vpcEndpointId":"({vpc}[^"]+)""",
      """"+requestParameters":\{("[^,]+,)*"roleSessionName\\?":\s*\\?"({session_name}[^"]+?)\\?"""",
      """"assumedRoleId\\?":\s*\\?"({assumedRoleId}[^"]+?)\\?"""",
      """"accessKeyId":"({key_id}[^"]+?)"""",
      """"+requestParameters[^\}]*?roleArn\\?"+:\s*\\?"({role_arn}[^"]+\/({role_name}[^"]+))\\?"+""",
      """"+requestParameters":\{("[^,]+,)*"roleSessionName\\?":\s*\\?"({session_name}[^"]+?)\\?"""",
      """"+responseElements":\{"credentials":\{("[^,]+,)*"expiration\\?":\s*\\?"({session_expiration}[^"]+?)\\?"""", 
      """"assumedRoleUser":\{("[^,]+,)*"arn"\s*:\s*"({session_arn}[^"]+)\\?""""
      """"recipientAccountId"+\s*:\s*"({object}[^"]+)""""
  ]
  ParserVersion = v1.0.0
  DupFields = ["role_name->account","assumedRoleId->role_id","result->failure_code"]

aws-cloudtrail-user-template = {
    Fields = [
      """\Wsuser=[^=]*?(({email_address}[^@=\s\/:]+@[^=\.\s\/:]+\.[^\s=\/:]+?)|({user}[\w\.\-]{1,40}\$?)(@[^=]+?)?)(\s+\w+=|\s*$)""",
      """\\?"type\\?":\\?"IAMUser\\?"[^\}]+?"userName\\?":\s*\\?"(({email_address}[^"@]+@[^"\.]+\.[^"]+)|({user}[\w\.\-]{1,40}\$?)(@({domain}[^@"]+))?)\\?"""",
      """"userIdentity\\?":.+?"arn\\?":\s*\\?"arn:aws:sts::\d+:assumed-role\/([^\/"]+\/)(AssumeRoleSession|((?![\w\-\.]{30,})(({email_address}[^"@]+@[^"\.]+\.[^"]+)|({user}[\w\.\-]{1,40}\$?)(@({domain}[^@"]+))?)))\\?"""",
      """"sourceIdentity\\?":\s*\\?"(({email_address}[^"@]+@[^"\.]+\.[^"]+)|({user}[\w\.\-]{1,40}\$?)(@({domain}[^@"]+))?)\\?"""",
      """"userIdentity\\?":.+?"AssumedRole\\?".+?"principalId\\?":\s*\\?"[A-Z\d]{1,50}:({email_address}[^"]+?@[^@"]+)\\?"\s*[,\]\}]""",
      """"userIdentity\\?":.+?"AssumedRole\\?".+?"sessionIssuer\\?":\s*\{[^\}]+?"IAMUser\\?"[^\}]+?"userName\\?":\s*\\?"(({email_address}[^"@]+@[^"\.]+\.[^"]+)|({user}[\w\.\-]{1,40}\$?)(@({domain}[^@"]+))?)\\?"""",
      """"userIdentity\\?":.+?"IAMUser\\?".+?"userName\\?":\s*\\?"(({email_address}[^"@]+@[^"\.]+\.[^"]+)|({user}[\w\.\-]{1,40}\$?)(@({domain}[^@"]+))?)\\?"""",
      """"userIdentity\\?":\s*\{.*?"type\\?":\s*\\?"({user}Root)\\?""""
    
}
```