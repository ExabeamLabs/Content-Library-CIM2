#### Parser Content
```Java
{
Name = amazon-awscloudtrail-json-app-activity-success-getrolecredentials
	ParserVersion = v1.0.0
	Conditions = [ """"eventName":""", """"GetRoleCredentials"""", """"eventType":""", """"AwsServiceEvent"""" ]
	Fields = ${AwsParserTemplates.aws-cloudtrail-json-2.Fields}[
    """exa_json_path=$.serviceEventDetails.account_id,exa_field_name=account_id""",
    """exa_json_path=$.sourceIPAddress,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """exa_json_path=$.userAgent,exa_field_name=user_agent""",
    """exa_json_path=$.userIdentity.userName,exa_regex=(({aws_email_address}({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|({aws_account}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))""",
    """exa_json_path=$.readOnly,exa_field_name=readonly""",
  ]

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