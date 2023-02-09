#### Parser Content
```Java
{
Name = amazon-awscloudtrail-json-policy-modify-success-createpolicyversion
  TimeFormat = """yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"""
  Conditions = [ """AwsApiCall""", """"eventName":"CreatePolicyVersion"""" ]
  Fields = ${AwsParserTemplates.aws-cloudtrail-json.Fields}[
  """"+requestParameters":\{("[^,]+,)*"policyArn\\?":\s*\\?"({policy_arn}[^"]+?\/({policy_name}[^"]+))\\?"""",
  """"+requestParameters":\{("[^,]+,)*"policyArn\\?":\s*\\?"({policy_arn}[^"]+?)\\?"""",
  """"+policyDocument"+:\s*"+\{[^\[]+({policy_content}"+Statement\\?"+.+\])\s*(?:\\n)?\s*\}"+""",
  """"+Effect\\?":\s*\\?"Allow\\?".+?Action\\?":\s*\[?({allowed_permissions}[^\.\]\}]+)\]?""",
  """"+Effect\\?":\s*\\?"Allow\\?".+?Resource\\?":\s*\[?({allowed_resources}[^\.\]\}]+)\]?""",
  """"+Effect\\?":\s*\\?"Deny\\?".+?Action\\?":\s*\[?({denied_permissions}[^\.\]\}]+)\]?""",
  """"+Effect\\?":\s*\\?"Deny\\?".+?Resource\\?":\s*\[?({denied_resources}[^\.\]\}]+)\]?""",
  """"+requestParameters":\{("[^,]+,)*"setAsDefault\\?":\s*\\?"?({set_as_defualt}[^"\}\s]+)\\?""",
  """"+responseElements":\{"policy":\{("[^,]+,)*"versionId\\?":\s*\\?"({policy_version_id}[^"]+?)\\?"""",
  ]
  ParserVersion = v1.0.0

aws-cloudtrail-json = {
    Vendor = Amazon
    Product = AWS CloudTrail
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
    Fields = [
      """"userIdentity":\{("[^,]+,)*"type"\\?:\s*\\?"({user_type}[^"]+?)\\?"""",
      """"userIdentity":\{("[^,]+,)*"type"\\?:\s*\\?"({user}Root)\\?"""",
      """"userIdentity":\{("[^,]+,)*"type"\\?:\s*\\?"[^"]+","principalId\\?"+\s*:\s*\\?"+?[^:@]+:?({user}[^@"\s]+)@?({domain}[^@"\s]+)?""""
      """"userIdentity":\{("[^,]+,)*"arn"\\?:\s*\\?"({user_arn}[^"]+?)\\?"""",
      """"userIdentity":\{("[^,]+,)*"accountId\\?"+\s*:\s*\\?"+?({aws_account}[^"]+?)\\?"+\s*[,\]\}]""",
      """"userIdentity":\{("[^,]+,)*"principalId\\?"+\s*:\s*\\?"+?({principal_id}[^"]+?)\\?"+\s*[,\]\}]""",
      """"userIdentity":\{("[^,]+,)*"attributes":\{("[^,]+,)*"mfaAuthenticated"\\?:\s*\\?"({mfa}[^"]+?)\\?"""",
      """"assumedRoleUser":\{("[^,]+,)*"arn"\s*:\s*"({assumed_role_arn}[^"]+)\\?""""
      """"eventTime"+\s*:\s*"+?(|({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)Z?)"+\s*[,\]\}]""",
      """"eventSource"+\s*:\s*"+?(|({service_name}[^"]+))"+\s*[,\]\}]""",
      """"eventName"+\s*:\s*"+?(|({operation}[^"]+))"+\s*[,\]\}]""",
      """"awsRegion"\s*:\s*"({region}[^"]+)"""",
      """"sourceIPAddress"+\s*:\s*"+?(?:({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({src_host}[^"]+))"+\s*[,\]\}]""",
      """"userAgent"\s*:\s*"\[?(|({user_agent}[^"]+?))\]?"""",
      """"eventID\\?"+:\\?"+({event_code}[^"\\]+)\\?"""",
      """"eventType"+\s*:\s*"+?(|({event_category}[^"]+))"+\s*[,\]\}]""",
      """"errorCode"\s*:\s*"({result}[^"]+)"""",
      """"errorMessage"\s*:\s*"({failure_reason}[^"]+)"""",
      """"readOnly"\s*:\s*({readonly}[^",}]+)""",
      """"vpcEndpointId":"({vpc}[^"]+)""",
      """"+userIdentity.+?AssumedRole.+?principalId\\?"+\s*:\s*\\?"+?[A-Z\d]+:({user}[^"]+@({domain}[^@"]+))\\?"+\s*[,\]\}]"""
      """"+requestParameters":\{("[^,]+,)*"roleSessionName\\?":\s*\\?"({session_name}[^"]+?)\\?"""",
      """"+responseElements":\{"assumedRoleUser":\{("[^,]+,)*"assumedRoleId\\?":\s*\\?"({assumedRoleId}[^"]+?)\\?"""",
      """"credentials":\{"accessKeyId":"({accessKeyId}[^"]+?)\\?""""
      """"userName"\\?:\s*\\?"({user}[^"]+@({domain}[^@"]+)|[^"]+)\\?"""",
      """\ssuser=([^\/=]+\/[^\/=]+\/)?({user}[^@"\s]+)@?({domain}[^@"\s]+)?"""
    
}
```