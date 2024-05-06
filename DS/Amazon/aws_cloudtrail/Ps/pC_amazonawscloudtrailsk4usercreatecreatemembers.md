#### Parser Content
```Java
{
Name = amazon-awscloudtrail-sk4-user-create-createmembers
  ParserVersion = v1.0.0
  Vendor = Amazon
  Product = AWS CloudTrail
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """"source":"aws.guardduty"""", """"eventName":""", """"CreateMembers"""" ]
  Fields = ${AmazonParsersTemplates.aws-cloudtrail-user-template.Fields}[
    """"eventTime":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)"""",
    """"sourceIPAddress":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """({event_name}CreateMembers)""",
    """"userAgent":"({user_agent}[^"]+)""",
    """"eventType":"({alert_type}[^"]+)""",
    """"eventID":"({alert_id}[^"]+)""",
    """({alert_name}CreateMembers)""",
    """"result":"[^"]*({action}rejected)""",
    """CreateMembers[^=]+?result":"({additional_info}[^"]+)""",
    """CreateMembers[^=]+?accountId":"({account_id}\d+)"""
  ]

aws-cloudtrail-user-template = {
    Fields = [
      """\Wsuser=[^=]*?(({aws_email_address}({email_address}[^@=\s\/:]+@[^=\.\s\/:]+\.[^\s=\/:]+?))|({aws_user}({user}[\w\.\-]{1,40}\$?)(@[^=]+?)?))(\s+\w+=|\s*$)""",
      """\\?"type\\?":\\?"IAMUser\\?"[^\}]+?"userName\\?":\s*\\?"(({aws_email_address}({email_address}[^"@]+@[^"\.]+\.[^"]+))|({aws_user}({user}[\w\.\-]{1,40}\$?))(@({domain}[^@"]+))?)\\?"""",
      """"userIdentity\\?":.+?"arn\\?":\s*\\?"arn:aws:sts::\d+:assumed-role\/([^\/"]+\/)(AssumeRoleSession|((?![\w\-\.]{30,})(({aws_email_address}[^"@]+@[^"\.]+\.[^"]+)|({aws_user}[\w\.\-]{1,40}\$?)(@({domain}[^@"]+))?)))\\?"""",
      """"sourceIdentity\\?":\s*\\?"(({aws_email_address}({email_address}[^"@]+@[^"\.]+\.[^"]+))|({aws_user}({user}[\w\.\-]{1,40}\$?))(@({domain}[^@"]+))?)\\?"""",
      """"userIdentity\\?":.+?"AssumedRole\\?".+?"principalId\\?":\s*\\?"[A-Z\d]{1,50}:({aws_email_address}[^"]+?@[^@"]+)\\?"\s*[,\]\}]""",
      """"userIdentity\\?":.+?"AssumedRole\\?".+?"sessionIssuer\\?":\s*\{[^\}]+?"IAMUser\\?"[^\}]+?"userName\\?":\s*\\?"(({aws_email_address}({email_address}[^"@]+@[^"\.]+\.[^"]+))|({aws_user}({user}[\w\.\-]{1,40}\$?))(@({domain}[^@"]+))?)\\?"""",
      """"userIdentity\\?":.+?"IAMUser\\?".+?"userName\\?":\s*\\?"(({aws_email_address}({email_address}[^"@]+@[^"\.]+\.[^"]+))|({aws_user}({user}[\w\.\-]{1,40}\$?))(@({domain}[^@"]+))?)\\?"""",
      """"userIdentity\\?":\s*\{.*?"type\\?":\s*\\?"({aws_user}({user}Root))\\?""""
    
}
```