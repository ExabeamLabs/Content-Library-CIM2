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
    TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ","yyyy-MM-dd'T'HH:mm:ssZ","yyyy-MM-dd'T'HH:mm:ss"]
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
      """"arn\\?":\s*\\?"arn:aws:sts::\d+:assumed-role\/({role}[^\/"]+)\/(AssumeRoleSession|((?![\w\-\.]{30,})(({aws_email_address}[^"@]+@[^"\.]+\.[^"]+)|({aws_user}[\w\.\-]{1,40}\$?)(@({domain}[^@"]+))?)))\\?"""",
      """"sourceIdentity\\?":\s*\\?"(({aws_email_address}({email_address}[^"@]+@[^"\.]+\.[^"]+))|({aws_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))(@({domain}[^@"]+))?)\\?"""",
      ""","userIdentity\\?":\{[^\}]+"AssumedRole\\?"[^\}]+"principalId\\?":\s*\\?"[A-Z\d]{1,25}:({aws_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))\\?"\s*[,\]\}]""",
      ""","userIdentity\\?":[^\}]+"IAMUser\\?"[^\}]+"userName\\?":\s*\\?"(({aws_email_address}({email_address}[^"@]+@[^"\.]+\.[^"]+))|({aws_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))(@({domain}[^@"]+))?)\\?"""",
      ""","userIdentity\\?":\s*\{[^\}]+"type\\?":\s*\\?"({aws_user}({user}Root))\\?""""
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
      """exa_regex="userAgent"\s*:\s*"\[?(|({user_agent}[^"]+?))\]?"""",
      """exa_json_path=$..eventType,exa_field_name=event_category""",
      """exa_json_path=$..eventID,exa_field_name=event_id""",
      """exa_json_path=$..errorCode,exa_field_name=result""",
      """exa_json_path=$..errorMessage,exa_field_name=failure_reason""",
      """exa_json_path=$..readOnly,exa_field_name=readonly""",
      """exa_json_path=$..vpcEndpointId,exa_field_name=vpc""",
      #"""exa_json_path=$.userIdentity.userName,exa_regex=(({aws_email_address}({email_address}[^"@]+@[^"\.]+\.[^"]+))|({aws_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))(@({domain}[^@"]+))?)\\?,exa_match_expr=Contains(toLower($.userIdentity.type),"iamuser")""",
      """exa_json_path=$.userIdentity,exa_regex="type\\?":\\?"IAMUser\\?"[^\}]+?"userName\\?":\s*\\?"(({aws_email_address}({email_address}[^"@]+@[^"\.]+\.[^"]+))|({aws_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))(@({domain}[^@"]+))?)\\?"""",
      """exa_regex="arn":\s*"arn:aws:sts::\d+:assumed-role\/({role}[^\/"]+)\/(AssumeRoleSession|\d{19}"|((?![\w\-\.]{30,})(({aws_email_address}[^"@]+@[^"\.]+\.[^"\s]+)|({aws_user}[\w\.\-]{1,40}\$?)(@({domain}[^@"]+))?)))\\?""",
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
      """exa_json_path=$.UserIdentityType,exa_field_name=user_type""",
      """exa_json_path=$.UserIdentityArn,exa_field_name=user_arn""",
      """exa_json_path=$.UserIdentityArn,exa_regex=role\/({role}[^\/"]+)\/?""",
      """exa_json_path=$.UserIdentityAccountId,exa_field_name=aws_account""",
      """exa_json_path=$.UserIdentityPrincipalid,exa_field_name=principal_id""",
      """exa_json_path=$..EventSource,exa_field_name=service_name""",
      """exa_json_path=$..EventName,exa_field_name=operation""",
      """exa_json_path=$.AWSRegion,exa_field_name=region""",
      """exa_json_path=$..SourceIpAddress,exa_regex=(?:({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?|({src_host}[\w\-.]+))$""",
      """exa_json_path=$..UserAgent,exa_regex=\[?({user_agent}[^\]]+)\]?$""",
      """exa_json_path=$..EventTypeName,exa_field_name=event_category""",
      """exa_json_path=$..AwsEventId,exa_field_name=event_id""",
      """exa_json_path=$..ErrorCode,exa_field_name=result""",
      """exa_json_path=$..ErrorMessage,exa_field_name=failure_reason""",
      """exa_json_path=$..ReadOnly,exa_field_name=readonly""",
      """exa_json_path=$..VpcEndpointId,exa_field_name=vpc""",
      """exa_json_path=$.UserIdentityType,exa_regex=({aws_user}({user}Root))""",
      """exa_json_path=$.RequestParameters.BucketName,exa_field_name=bucket_name""",
      """exa_json_path=$.RequestParameters.Host,exa_field_name=bucket_host""",
      """exa_json_path=$.Resources..ARN,exa_field_name=bucket_arn"""
      """exa_json_path=$.UserIdentityAccessKeyId,exa_field_name=key_id"""
      """exa_json_path=$..RecipientAccountId,exa_field_name=aws_account"""
      """exa_regex=RequestParameters":"({additional_info}.+?),"\w+"?:"""
    
}
```