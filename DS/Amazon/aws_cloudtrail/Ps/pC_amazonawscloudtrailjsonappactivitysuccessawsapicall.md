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
  Fields = ${AmazonParsersTemplates.aws-cloudtrail-user-template.Fields}[
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
    """bucketName\\?"+:\\?"+({object}[^\\]+)\\?""""
    """assumed-role({role}.+?)\\""""
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