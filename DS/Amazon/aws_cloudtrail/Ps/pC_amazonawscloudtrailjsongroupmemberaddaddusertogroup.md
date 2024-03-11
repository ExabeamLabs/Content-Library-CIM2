#### Parser Content
```Java
{
Name = amazon-awscloudtrail-json-group-member-add-addusertogroup
  Vendor = Amazon
  Product = AWS CloudTrail
  TimeFormat = """yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"""
  ParserVersion = "v1.0.0"
  Conditions = [ """AwsApiCall""", """"eventName":"AddUserToGroup"""" ] 
  Fields = ${AwsParserTemplates.aws-cloudtrail-json.Fields}[
  """"+requestParameters.+?groupName\\?":\s*\\?"({group_name}[^"]+?)\\?"""",
  """"+requestParameters.+?userName\\?":\s*\\?"({identity}[^"]+?)\\?"""",
  ]
},  

{
  Name = amazon-awscloudtrail-json-endpoint-create-runinstances
  Vendor = Amazon
  Product = AWS CloudTrail
  ParserVersion = "v1.0.0"
  TimeFormat = """yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"""
  Conditions = [ """AwsApiCall""", """"eventName":"RunInstances"""" ] 
  Fields = ${AwsParserTemplates.aws-cloudtrail-json.Fields}[
  """"+requestParameters.+?imageId\\?":\s*\\?"({source_resource}[^"]+?)\\?"""",
  """"+requestParameters.+?keyName\\?":\s*\\?"({key_name}[^"]+?)\\?"""",
  """"+requestParameters.+?instanceType\\?":\s*\\?"({instance_type}[^"]+?)\\?"""",
  """"+iamInstanceProfile.+?arn\\?":\s*\\?"({instance_profile_arn}[^"]+?)\\?"""",
  """"+responseElements.+?instanceId\\?":\s*\\?"({resource_id}[^"]+?)\\?"""",
  """"+responseElements.+?privateDnsName\\?":\s*\\?"({new_host}[^"]+?)\\?"""",
  """"+responseElements.+?availabilityZone\\?":\s*\\?"({availabilty_zone}[^"]+?)\\?"""",
  """"+responseElements.+?privateIpAddress\\?":\s*\\?"({new_ip}[^"]+?)\\?"""",
  """"+responseElements.+?groupName\\?":\s*\\?"({security_group}[^"]+?)\\?"""",
  ]

aws-cloudtrail-json = {
    Vendor = Amazon
    Product = AWS CloudTrail
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
    Fields = [
      """"userIdentity":\{("[^,]+,)*"type"\\?:\s*\\?"({user_type}[^"]+?)\\?"""",
      """"userIdentity":\{("[^,]+,)*"type"\\?:\s*\\?"({user}Root)\\?"""",
      """"userIdentity":\{("[^,]+,)*"arn"\\?:\s*\\?"({user_arn}[^"]+?)\\?"""",
      """"userIdentity":\{("[^,]+,)*"accountId\\?"+\s*:\s*\\?"+?({aws_account}[^"]+?)\\?"+\s*[,\]\}]""",
      """"userIdentity":\{("[^,]+,)*"principalId\\?"+\s*:\s*\\?"+?({principal_id}[^"]+?)\\?"+\s*[,\]\}]""",
      """"userName"\\?:\s*\\?"(({email_address}[^"@]+@[^"\.]+\.[^"]+)|({user}[^"]+)(@({domain}[^@"]+))?)\\?"""",
      """\Wsuser=[^=]*?(({email_address}[^@=\s\/:]+@[^=\.\s\/:]+\.[^\s=\/:]+?)|({user}[^\\\/@=]+)@[^=]+?)(\s+\w+=|\s*$)""",
      """"userIdentity":\{("[^,]+,)*"attributes":\{("[^,]+,)*"mfaAuthenticated"\\?:\s*\\?"({mfa}[^"]+?)\\?"""",
      """"assumedRoleUser":\{("[^,]+,)*"arn"\s*:\s*"({assumed_role_arn}[^"]+)\\?""""
      """"eventTime"+\s*:\s*"+?(|({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)Z?)"+\s*[,\]\}]""",
      """"eventSource"+\s*:\s*"+?(|({service_name}[^"]+))"+\s*[,\]\}]""",
      """"eventName"+\s*:\s*"+?(|({operation}[^"]+))"+\s*[,\]\}]""",
      """"awsRegion"\s*:\s*"({region}[^"]+)"""",
      """"sourceIPAddress"+\s*:\s*"+?(?:({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?|({src_host}[^"]+))"+\s*[,\]\}]""",
      """"userAgent"\s*:\s*"\[?(|({user_agent}[^"]+?))\]?"""",
      """"eventID\\?"+:\\?"+({event_code}[^"\\]+)\\?"""",
      """"eventType"+\s*:\s*"+?(|({event_category}[^"]+))"+\s*[,\]\}]""",
      """"errorCode"\s*:\s*"({result}[^"]+)"""",
      """"errorMessage"\s*:\s*"({failure_reason}[^"]+)"""",
      """"readOnly"\s*:\s*({readonly}[^",\}]+)("|,|\}\s*$)""",
      """"vpcEndpointId":"({vpc}[^"]+)""",
      """"+userIdentity.+?AssumedRole.+?principalId\\?"+\s*:\s*\\?"+?[A-Z\d]+:(({email_address}[^"@]+@[^"\.]+\.[^"]+)|({user}[^"]+)(@({domain}[^@"\.]+)))\\?"+\s*[,\]\\\\\}]"""
      """"+requestParameters":\{("[^,]+,)*"roleSessionName\\?":\s*\\?"({session_name}[^"]+?)\\?"""",
      """"+responseElements":\{"assumedRoleUser":\{("[^,]+,)*"assumedRoleId\\?":\s*\\?"({assumedRoleId}[^"]+?)\\?"""",
      """"credentials":\{"accessKeyId":"({accessKeyId}[^"]+?)\\?""""
      """"userIdentity".+?"type":"(user|User|IAMUser)".+?""userName"\\?:\s*\\?"({user}[^"]+@({domain}[^@"]+)|[^"]+)\\?"""",
      """"userIdentity".+?"type":"(user|User|IAMUser)".+?"userName"\\?:\s*\\?"(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[^"]+)(@({domain}[^@"]+))?)\\?"""",
      """"userIdentity\\?".+?"arn\\?"\s*:\s*\\?"?arn:aws:sts::\d+:assumed-role\/([^\/"]+\/)(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[^"]+))"""
      """\ssuser=([^\/=]+\/[^\/=]+\/)?({user}[^@"\s]+)@?({domain}[^@"\s]+)?"""
    
}
```