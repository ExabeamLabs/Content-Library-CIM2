#### Parser Content
```Java
{
Name = "amazon-awscloudtrail-json-app-activity-success-awsapicall"
  Vendor = "Amazon"
  Product = "AWS CloudTrail"
  ExtractionType = json
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [
    """AwsApiCall\"""
    """logSource"""
  ]
  Fields = ${AmazonParsersTemplates.aws-cloudtrail-user-template.Fields}[
    """exa_json_path=$.log.timestamp,exa_field_name=time""",
    """exa_json_path=$.log.resource.labels.project_id,exa_field_name=project_id""",
    """exa_json_path=$.log.logName,exa_field_name=logName""",
    """exa_json_path=$.log.textPayload,exa_regex=\\?"+eventSource\\?"+\s*:\s*\\?"+?(|({host}[\w\-\.]+))\\?"+\s*[,\]\}]""",
    """exa_json_path=$.log.textPayload,exa_regex="+eventName\\?"+:\\?"+({operation}[^"\\]+)\\?"""",
    """exa_json_path=$.log.textPayload,exa_regex="+eventSource\\\?"+:\\?"+({service_name}[^"\\]+)\\?"""",
    """exa_json_path=$.log.textPayload,exa_regex="+eventType\\?"+:\\?"+({app}[^"\\]+)\\?"""",
    """exa_json_path=$.log.textPayload,exa_regex="+accountId\\?"+:\\?"+({account_id}[^"\\]+)\\?"""",
    """exa_json_path=$.log.textPayload,exa_regex="+eventID\\?"+:\\?"+({event_log_id}[^"\\]+)\\?"""",
    """exa_json_path=$.log.textPayload,exa_regex="+sourceIPAddress\\?"+:\\?"+(({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({src_host}[^"\\]+))\\?"""",
    """exa_json_path=$.log.textPayload,exa_regex="+userAgent\\?"+:\\?"+({user_agent}[^"\\]+)\\?"""",
    """exa_json_path=$.log.textPayload,exa_regex=userIdentity.+?"+type\\?"+:\\?"+({user_type}[^"\\]+)\\?"""",
    """exa_json_path=$.log.textPayload,exa_regex=bucketName\\?"+:\\?"+({object}[^\\"]+)\\?"""",
    """exa_json_path=$.log.textPayload,exa_regex=assumed-role({role}.+?)\\""""
  ]
  ParserVersion = "v1.0.0"

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