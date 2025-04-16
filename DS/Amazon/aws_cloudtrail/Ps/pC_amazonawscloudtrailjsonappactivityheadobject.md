#### Parser Content
```Java
{
Name = amazon-awscloudtrail-json-app-activity-headobject
	ParserVersion = v1.0.0
	Conditions = [ """"eventName":"HeadObject"""", """"resources":""", """"eventType":""", """"awsRegion":""" ]
	Fields = ${AwsParserTemplates.aws-cloudtrail-json-2.Fields}[
      """exa_json_path=$.sourceIPAddress,exa_regex=^(\s*|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)$"""
     """exa_json_path=$.errorMessage,exa_field_name=failure_reason""",
      """exa_json_path=$.errorCode,exa_field_name=result""",
     """exa_json_path=$.resources,exa_regex=[^\]]+?Object[^\}]+?(?:ARN|arn)\\?":\s*\\?"({file_arn}[^"]+)""",
     """exa_json_path=$.resources,exa_regex=[^\]]+?Bucket[^\}]+?(?:ARN|arn)\\?":\s*\\?"({bucket_arn}[^"]+)""",
     """exa_json_path=$.resources,exa_field_name=additional_info"""    
      """exa_json_path=$.userIdentity,exa_regex="type\\?":\\?"IAMUser\\?"[^\}]+?"userName\\?":\s*\\?"(({aws_email_address}({email_address}[^"@]+@[^"\.]+\.[^"]+))|({aws_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))(@({domain}[^@"]+))?)\\?"""",
      """exa_json_path=$.userIdentity.arn,exa_regex=arn:aws:sts::\d+:assumed-role\/({role}[^\/"]+)\/(AssumeRoleSession|((?![\w\-\.]{30,})(({aws_email_address}[^"@]+@[^"\.]+\.[^"]+)|({aws_user}[\w\.\-]{1,40}\$?)(@({domain}[^@"]+))?)))\\?""",
      """exa_json_path=$.userIdentity.type,exa_regex=({aws_user}({user}Root))""",
      """exa_json_path=$.userIdentity.accessKeyId,exa_field_name=key_id"""
      """exa_json_path=$.userIdentity.accountId,exa_field_name=aws_account""",
      """exa_json_path=$.userIdentity.principalId,exa_field_name=principal_id""",
      """exa_json_path=$.userIdentity.type,exa_field_name=user_type""",
      """exa_json_path=$.userIdentity.arn,exa_field_name=user_arn""",
      """exa_json_path=$.userIdentity.arn,exa_regex=role\/({role}[^\/"]+)\/?""",
      """exa_json_path=$..userIdentity..attributes.mfaAuthenticated,exa_field_name=mfa""",
      """exa_json_path=$..vpcEndpointId,exa_field_name=vpc"""
  ]
  DupFields = [ "event_name->operation" ]  

aws-cloudtrail-json-2 = {
  Vendor = Amazon
  Product = AWS CloudTrail
  ExtractionType = json
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Fields = [
  """exa_json_path=$.eventTime,exa_field_name=time""",
  """exa_json_path=$.destinationServiceName,exa_field_name=app""",
  """exa_json_path=$.eventSource,exa_field_name=src_host""",
  """exa_json_path=$.eventName,exa_field_name=event_name""",
  """exa_json_path=$.eventType,exa_field_name=event_category""",
  """exa_json_path=$.eventID,exa_field_name=alert_id""",
  """exa_json_path=$.awsRegion,exa_field_name=region""",
  """exa_json_path=$.eventCategory,exa_field_name=event_category""",
  """exa_json_path=$.recipientAccountId,exa_field_name=aws_account"""
  
}
```