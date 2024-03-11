#### Parser Content
```Java
{
Name = amazon-awscloudtrail-json-file-write-putobject
  Vendor = Amazon
  Product = AWS CloudTrail
  TimeFormat = """yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"""
  ParserVersion = "v1.0.0"
  Conditions = [ """AwsApiCall""", """"eventName":"PutObject"""" ] 
  Fields = ${AwsParserTemplates.aws-cloudtrail-json.Fields}[
  """"+requestParameters.+?bucketName\\?":\s*\\?"({bucket_name}[^"]+?)\\?"""",
  """"+requestParameters.+?Host\\?":\s*\\?"({bucket_host}[^"]+?)\\?"""",
  """"+requestParameters.+?key\\?":\s*\\?"({file_path}[^"]+?)\\?"""",
  """"+additionalEventData.+?bytesTransferredIn\\*":\s*({bytes_in}\d+)""",
  """"+resources.+?Object.+?(?:ARN|arn)\\?":\s*\\?"({file_arn}[^"]+?)\\?"""",
  """"+resources.+?Bucket.+?(?:ARN|arn)\\?":\s*\\?"({bucket_arn}[^"]+?)\\?"""",
  ]
} 

{
  Name = amazon-awscloudtrail-json-image-create-awsapicall
  Vendor = Amazon
  Product = AWS CloudTrail
  ParserVersion = "v1.0.0"
  TimeFormat = """yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"""
  Conditions = [ """AwsApiCall""", """"eventName":"CreateImage"""" ] 
  Fields = ${AwsParserTemplates.aws-cloudtrail-json.Fields}[
  """"+requestParameters.+?({source_resource_type}[Ss]napshot|[Ii]nstance)Id\\?":\s*\\?"({source_resource}[^",]+?)\\?"""",
  """"+requestParameters.+?name\\?":\s*\\?"({image_name}[^"]+?)\\?"""",
  """"+requestParameters.+?[Dd]escription\\?":\s*\\?"({description}[^"]+?)\\?"""",
  """"+responseElements.+?imageId\\?":\s*\\?"({resource_id}[^"]+?)\\?"""",
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