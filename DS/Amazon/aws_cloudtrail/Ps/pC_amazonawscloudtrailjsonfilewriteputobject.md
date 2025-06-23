#### Parser Content
```Java
{
Name = amazon-awscloudtrail-json-file-write-putobject
  Vendor = Amazon
  Product = AWS CloudTrail
  # TimeFormat = """yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"""
  ParserVersion = "v1.0.0"
  Conditions = [ """AwsApiCall""", """"eventName":""", """"PutObject"""" ] 
  Fields = ${AwsParserTemplates.aws-cloudtrail-json.Fields}[
  """"requestParameters":[^\}]*?"key\\?":\\?"({file_path}(({file_dir}[^\"]+?)[\\\/]+?)?({file_name}[^"\\\/]+?(\.({file_ext}[^\.\"\\\/]+))?)?)\\?""""
  """"resources":[^\]]+?Object[^\}]+?(?:ARN|arn)\\?":\s*\\?"({file_arn}[^"]+)\\?""""
  """"resources":[^\]]+?Bucket[^\}]+?(?:ARN|arn)\\?":\s*\\?"({bucket_arn}[^"]+)\\?""""
  """"additionalEventData":.+?"bytesTransferredIn\\?":({bytes_in}\d+)"""
  """"additionalEventData":.+?"bytesTransferredOut\\?":({bytes_out}\d+)"""
  """exa_json_path=$.requestParameters,exa_regex="key\\?":\\?"({file_path}(({file_dir}[^\"]+?)[\\\/]+?)?({file_name}[^"\\\/]+?(\.({file_ext}[^\.\"\\\/]+))?)?)\\?""""
  """exa_json_path=$.resources,exa_regex=Object.+?(?:ARN|arn)\\?":\s*\\?"({file_arn}[^"]+)\\?"""
  """exa_json_path=$.additionalEventData.bytesTransferredIn,exa_field_name=bytes_in"""
  """exa_json_path=$.additionalEventData.bytesTransferredOut,exa_field_name=bytes_out"""
  """exa_json_path=$.resources,exa_regex=Bucket.+?(?:ARN|arn)\\?":\s*\\?"({bucket_arn}[^"]+)\\?"""
  ]
} 

{
  Name = amazon-awscloudtrail-json-file-write-success-putobject
  Vendor = Amazon
  Product = AWS CloudTrail
  TimeFormat = """yyyy-MM-dd'T'HH:mm:ssZ"""
  ParserVersion = "v1.0.0"
  ExtractionType = json
  Conditions = [ """"source":"aws.s3"""", """"PutObject"""", """"resources":""" ] 
  Fields = [
    """exa_json_path=$.time,exa_field_name=time""",
    """exa_json_path=$.detail.reason,exa_field_name=operation""",
    """exa_json_path=$.detail.source-ip-address,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """exa_json_path=$.detail.object.key,exa_field_name=object""",
    """exa_json_path=$.detail.bucket.name,exa_field_name=bucket_name""",
    """exa_json_path=$.region,exa_field_name=region""",
    """exa_json_path=$.account,exa_field_name=aws_account""",
    """exa_json_path=$.detail-type,exa_field_name=event_name""",
    """exa_json_path=$.account,exa_field_name=aws_account""",
    """exa_json_path=$.resources,exa_regex=[^\]]+?Object[^\}]+?(?:ARN|arn)\\?":\s*\\?"({file_arn}[^"]+)""",
    """exa_json_path=$.resources,exa_regex=[^\]]+?Bucket[^\}]+?(?:ARN|arn)\\?":\s*\\?"({bucket_arn}[^"]+)""",
    """exa_json_path=$.resources,exa_field_name=additional_info"""          
  ]
} 

${AwsParserTemplates.aws-cloudtrail-json}{
  Name = amazon-awscloudtrail-json-image-create-awsapicall
  Vendor = Amazon
  Product = AWS CloudTrail
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """AwsApiCall""", """"eventName":""", """"CreateImage"""" ] 
  Fields = ${AwsParserTemplates.aws-cloudtrail-json.Fields}[
      """exa_json_path=$.requestParameters,exa_regex=({src_resource_type}[Ss]napshot|[Ii]nstance)Id\\?":\s*\\?"({src_resource}[^",]+?)\\?""""
      """exa_json_path=$..requestParameters.name,exa_field_name=image_name"""
      """exa_json_path=$..description,exa_field_name=description"""
      """exa_json_path=$..imageId,exa_field_name=resource_id"""
  ]
  DupFields = [ "result->failure_code", "src_resource->source_resource", "src_resource_type->source_resource_type" ]

aws-cloudtrail-json = {
    Vendor = Amazon
    Product = AWS CloudTrail
    ExtractionType = json
    TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ","yyyy-MM-dd'T'HH:mm:ssZ"]
    Fields = [
      """"instanceId\\?":\\?"({instance_id}[^"]+?)\\?""""
      """"userIdentity":\{("[^,]+,)*"type"\\?:\s*\\?"({user_type}[^"]+?)\\?"""",
      """"userIdentity":\{("[^,]+,)*"arn"\\?:\s*\\?"({user_arn}[^"]+?)\\?"""",
      """"userIdentity":\{("[^,]+,)*"accountId\\?"+\s*:\s*\\?"+?({aws_account}[^"]+?)\\?"""",
      """"userIdentity":\{("[^,]+,)*"principalId\\?"+\s*:\s*\\?"+?({principal_id}[^"]+?)\\?"""",
      """"userIdentity":\{("[^,]+,)*"attributes":\{("[^,]+,)*"mfaAuthenticated"\\?:\s*\\?"({mfa}[^"]+?)\\?"""",
      """"assumedRoleUser":\{("[^,]+,)*"arn"\s*:\s*"({role_arn}[^"]+)\\?""""
      """"arn":\s*"[^"]*?role\/({role}[^\/"]+)[\/"]""",
      # """"eventTime"+\s*:\s*"+?(|({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)Z?)"+\s*[,\]\}]""",
      """"TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d\d\d\d\dZ)"""",
      """"eventTime"+\s*:\s*"+?(|({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ?))"""",
      """"eventSource"+\s*:\s*"+?(|({service_name}[^"]+))"""",
      """"eventName"+\s*:\s*"+?(|({operation}[^"]+))"""",
      """"awsRegion"\s*:\s*"({region}[^"]+)"""",
      """"sourceIPAddress"+\s*:\s*"+?(?:({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?|({src_host}[\w\-.]+))"+\s*[,\]\}]""",
      """"userAgent"\s*:\s*"\[?(|({user_agent}[^"]+?))\]?"""",
      """"eventID\\?"+:\\?"+({event_id}[^"\\]+)\\?"""",
      """"eventType"+\s*:\s*"+?(|({event_category}[^"]+))"""",
      """"errorCode"\s*:\s*"({result}[^"]+)"""",
      """"errorMessage"\s*:\s*"({failure_reason}[^"]+)"""",
      """"readOnly"\s*:\s*({readonly}[^",\}]+)("|,|\}\s*$)""",
      """"vpcEndpointId":"({vpc}[^"]+)""",
      """"+requestParameters":\{("[^,]+,)*"roleSessionName\\?":\s*\\?"({session_name}[^"]+?)\\?"""",
      """"+responseElements":\{"assumedRoleUser":\{("[^,]+,)*"assumedRoleId\\?":\s*\\?"({role_id}[^"]+?)\\?"""",
      """"accessKeyId":"({key_id}[^"]+?)"""",
      #AWS CloudTrail user regexes
      """\Wsuser=[^=]*?(({aws_email_address}({email_address}[^@=\s\/:]+@[^=\.\s\/:]+\.[^\s=\/:]+?))|({aws_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))(@[^=]+?)?)(\s+\w+=|\s*$)""",
      """\\?"type\\?":\\?"IAMUser\\?"[^\}]+?"userName\\?":\s*\\?"(({aws_email_address}({email_address}[^"@]+@[^"\.]+\.[^"]+))|({aws_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))(@({domain}[^@"]+))?)\\?"""",
      ""","userIdentity\\?":.+?,"arn\\?":\s*\\?"arn:aws:sts::\d+:assumed-role\/({role}[^\/"]+)\/(AssumeRoleSession|((?![\w\-\.]{30,})(({aws_email_address}[^"@]+@[^"\.]+\.[^"]+)|({aws_user}[\w\.\-]{1,40}\$?)(@({domain}[^@"]+))?)))\\?"""",
      """"sourceIdentity\\?":\s*\\?"(({aws_email_address}({email_address}[^"@]+@[^"\.]+\.[^"]+))|({aws_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))(@({domain}[^@"]+))?)\\?"""",
      ""","userIdentity\\?":.+?"AssumedRole\\?".+?"principalId\\?":\s*\\?"[A-Z\d]{1,25}:({aws_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))\\?"\s*[,\]\}]""",
      ""","userIdentity\\?":.+?"AssumedRole\\?".+?"sessionIssuer\\?":\s*\{[^\}]+?"IAMUser\\?"[^\}]+?"userName\\?":\s*\\?"(({aws_email_address}({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)))|({aws_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))(@({domain}[^@"]+))?)\\?"""",
      ""","userIdentity\\?":.+?"IAMUser\\?".+?"userName\\?":\s*\\?"(({aws_email_address}({email_address}[^"@]+@[^"\.]+\.[^"]+))|({aws_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))(@({domain}[^@"]+))?)\\?"""",
      ""","userIdentity\\?":\s*\{.*?"type\\?":\s*\\?"({aws_user}({user}Root))\\?""""
      """requestParameters":"({additional_info}.+?),"\w+"?:"""
      """"RestrictPublicBuckets\\*":({restrict_public_buckets}[^",\\\}]+)"""
      """"BlockPublicPolicy\\*":({block_public_policy}[^",\\\}]+)"""
      """"BlockPublicAcls\\*":({block_public_acls}[^",\\\}]+)"""
      """"IgnorePublicAcls\\*":({ignore_public_acls}[^",\\\}]+)"""
      """"Host\\*":\\*"({bucket_host}[^",\\\}]+)"""
      """"ARN\\*":\\*"({bucket_arn}[^",\\\}]+)"""
      """exa_json_path=$.userIdentity.type,exa_field_name=user_type""",
      """exa_json_path=$.userIdentity.arn,exa_field_name=user_arn""",
      """exa_json_path=$.userIdentity.arn,exa_regex=role\/({role}[^\/"]+)\/?""",
      """exa_json_path=$.userIdentity.accountId,exa_field_name=aws_account""",
      """exa_json_path=$.userIdentity.principalId,exa_field_name=principal_id""",
      """exa_json_path=$..userIdentity..attributes.mfaAuthenticated,exa_field_name=mfa""",
      """exa_json_path=$..TimeGenerated,exa_field_name=time""",
      """exa_json_path=$..eventTime,exa_field_name=time""",
      """exa_json_path=$..eventSource,exa_field_name=service_name""",
      """exa_json_path=$..eventName,exa_field_name=operation""",
      """exa_json_path=$.awsRegion,exa_field_name=region""",
      """exa_json_path=$..sourceIPAddress,exa_regex=(?:({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?|({src_host}[\w\-.]+))$""",
      """exa_json_path=$..userAgent,exa_regex=\[?({user_agent}.*?)\]?$""",
      """exa_json_path=$..eventType,exa_field_name=event_category""",
      """exa_json_path=$..eventID,exa_field_name=event_id""",
      """exa_json_path=$..errorCode,exa_field_name=result""",
      """exa_json_path=$..errorMessage,exa_field_name=failure_reason""",
      """exa_json_path=$..readOnly,exa_field_name=readonly""",
      """exa_json_path=$..vpcEndpointId,exa_field_name=vpc""",
      #"""exa_json_path=$.userIdentity.userName,exa_regex=(({aws_email_address}({email_address}[^"@]+@[^"\.]+\.[^"]+))|({aws_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))(@({domain}[^@"]+))?)\\?,exa_match_expr=Contains(toLower($.userIdentity.type),"iamuser")""",
      """exa_json_path=$.userIdentity,exa_regex="type\\?":\\?"IAMUser\\?"[^\}]+?"userName\\?":\s*\\?"(({aws_email_address}({email_address}[^"@]+@[^"\.]+\.[^"]+))|({aws_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))(@({domain}[^@"]+))?)\\?"""",
      """exa_json_path=$.userIdentity.arn,exa_regex=arn:aws:sts::\d+:assumed-role\/({role}[^\/"]+)\/(AssumeRoleSession|((?![\w\-\.]{30,})(({aws_email_address}[^"@]+@[^"\.]+\.[^"]+)|({aws_user}[\w\.\-]{1,40}\$?)(@({domain}[^@"]+))?)))\\?""",
      """exa_json_path=$.userIdentity.type,exa_regex=({aws_user}({user}Root))""",
      """exa_json_path=$.requestParameters.bucketName,exa_field_name=bucket_name""",
      """exa_json_path=$.requestParameters.Host,exa_field_name=bucket_host""",
      """exa_json_path=$.resources..ARN,exa_field_name=bucket_arn"""
      """exa_json_path=$.userIdentity.accessKeyId,exa_field_name=key_id"""
      """exa_json_path=$..requestParameters..InstanceId,exa_field_name=instance_id"""
      """exa_json_path=$..requestParameters..instanceId,exa_field_name=instance_id"""
      """exa_json_path=$..recipientAccountId,exa_field_name=aws_account"""
      """exa_regex=requestParameters":"({additional_info}.+?),"\w+"?:"""
      """exa_json_path=$..RestrictPublicBuckets,exa_field_name=restrict_public_buckets"""
      """exa_json_path=$..BlockPublicPolicy,exa_field_name=block_public_policy"""
      """exa_json_path=$..BlockPublicAcls,exa_field_name=block_public_acls"""
      """exa_json_path=$..IgnorePublicAcls,exa_field_name=ignore_public_acls"""
      """exa_json_path=$..Host,exa_field_name=bucket_host"""
      """exa_json_path=$..ARN,exa_field_name=bucket_arn"""
    
}
```