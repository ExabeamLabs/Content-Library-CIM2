#### Parser Content
```Java
{
Name = "amazon-awscloudtrail-json-app-activity-success-awsapicall"
Vendor = "Amazon"
Product = "AWS CloudTrail"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
  """AwsApiCall\"""
  """logSource"""
]
Fields = [
  """"+timestamp"+:"+({time}[^"]+)""""
  """({host}\d+),"""
  """"+project_id"+:"+({project_id}[^"]+)""""
  """"+logName"+:"+({logName}[^"]+)""""
  """"+eventName\\?"+:\\?"+({operation}[^"\\]+)\\?""""
  """"+eventSource\\\?"+:\\?"+({service_name}[^"\\]+)\\?""""
  """"+eventType\\?"+:\\?"+({app}[^"\\]+)\\?""""
  """"+accountId\\?"+:\\?"+({account_id}[^"\\]+)\\?""""
  """"+eventID\\?"+:\\?"+({event_log_id}[^"\\]+)\\?""""
  """"+sourceIPAddress\\?"+:\\?"+(({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({src_host}[^"\\]+))\\?""""
  """"+userAgent\\?"+:\\?"+({user_agent}[^"\\]+)\\?""""
  """userIdentity.+?"+type\\?"+:\\?"+({user_type}[^"\\]+)\\?""""
  """"+userName\\?"+:\\?"+({user}[^"\\]+)\\?""""
  """bucketName\\?"+:\\?"+({object}[^\\]+)\\?""""
  """assumed-role({role}.+?)\\""""
]
ParserVersion = "v1.0.0"


}
```