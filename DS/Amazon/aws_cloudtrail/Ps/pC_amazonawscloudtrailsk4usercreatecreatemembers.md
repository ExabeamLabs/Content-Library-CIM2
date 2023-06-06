#### Parser Content
```Java
{
Name = amazon-awscloudtrail-sk4-user-create-createmembers
  ParserVersion = v1.0.0
  Vendor = Amazon
  Product = AWS CloudTrail
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """"source":"aws.guardduty"""", """"eventName":"CreateMembers"""" ]
  Fields = ${AmazonParsersTemplates.aws-cloudtrail-user-template.Fields}[
    """"eventTime":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)"""",
    """"sourceIPAddress":"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
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
    """\Wsuser=[^=]*?(({email_address}[^@=\s\/:]+@[^=\.\s\/:]+\.[^\s=\/:]+?)|({user}[^\\\/@=]+?)(@[^=]+?)?)(\s+\w+=|\s*$)""",
    """\\?"type\\?":\\?"IAMUser\\?"[^\}]+?"userName\\?":\s*\\?"(({email_address}[^"@]+@[^"\.]+\.[^"]+)|({user}[^"]+?)(@({domain}[^@"]+))?)\\?"""",
    """"userIdentity\\?":.+?"arn\\?":\s*\\?"arn:aws:sts::\d+:assumed-role\/([^\/"]+\/)(AssumeRoleSession|((?![\w\-\.]{30,})(({email_address}[^"@]+@[^"\.]+\.[^"]+)|({user}[^"]+?)(@({domain}[^@"]+))?)))\\?"""",
    """"sourceIdentity\\?":\s*\\?"(({email_address}[^"@]+@[^"\.]+\.[^"]+)|({user}[^"]+?)(@({domain}[^@"]+))?)\\?"""",
    """"userIdentity\\?":.+?"AssumedRole\\?".+?"principalId\\?":\s*\\?"[A-Z\d]{1,50}:({email_address}[^"]+?@[^@"]+)\\?"\s*[,\]\}]""",
    """"userIdentity\\?":.+?"AssumedRole\\?".+?"sessionIssuer\\?":\s*\{[^\}]+?"IAMUser\\?"[^\}]+?"userName\\?":\s*\\?"(({email_address}[^"@]+@[^"\.]+\.[^"]+)|({user}[^"]+?)(@({domain}[^@"]+))?)\\?"""",
    """"userIdentity\\?":.+?"IAMUser\\?".+?"userName\\?":\s*\\?"(({email_address}[^"@]+@[^"\.]+\.[^"]+)|({user}[^"]+?)(@({domain}[^@"]+))?)\\?"""",
    """"userIdentity\\?":\s*\{.*?"type\\?":\s*\\?"({user}Root)\\?""""
  
}
```