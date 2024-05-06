#### Parser Content
```Java
{
Name = amazon-awscloudtrail-sk4-app-activity-success-redshift
  Vendor = Amazon
  Product = AWS CloudTrail
  TimeFormat = "epoch"
  Conditions = [ """CEF:""", """destinationServiceName =AWS""", """dproc=Redshift""" ]
  Fields = ${AmazonParsersTemplates.aws-cloudtrail-user-template.Fields}[
    """"date":"*({time}\d{13})"?""",
    """suid=({user_id}\S+)""",
    """"message":"({additional_info}[^"]+?)"""",
    """"severity":"({severity}[^"]+?)"""",
    """"eventId":"({event_name}[^"]+?)"""",
    """"eventCategories":\[?({categories}[^\]]+)\]?""",
    """dproc=({app}Redshift)""",
    """"sourceType":"({source_type}[^"]+?)"""",
    """"sourceIdentifier":"({src_host}[^"]+?)""""
  ]
  ParserVersion = "v1.0.0"

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