#### Parser Content
```Java
{
Name = microsoft-o365-sk4-app-activity-success-newinboxrule
  Vendor = Microsoft
  Product = Microsoft 365
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = ["""New-InboxRule""" ]
  Fields = [
    """time="({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
    """host="({host}[^"]+)"""",
    """"CreationTime":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""",
    """"Name":"ForwardTo".+?"Value":"(?:smtp:)?({target}[^"]+)""""
    """"ResultStatus":"({result}[^"]+)"""",
    """"ClientIP":"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """({operation}New-InboxRule)"""
    """cs1=(\[\{"additional-properties"\:)?\{"({operation}[^"]+)""",
    """msg=({additional_info}.+?)\s\w+=""",
    """user="({user}[^"]+)""",
    """user_email="({email_address}[^@"]+@[^\."]+\.[^"]+)"""",
    """"Value":"(?:smtp:)?.+?@({dest_domain}[^"]+)"""",
    """UserId":"({user}.+?@({domain}[^"]+).+?)""",
    """destinationServiceName =({app}.+?)\s*filePath""",
    """({app}Office 365)"""
    """"SubjectOrBodyContainsWords":"({filter_key_words}[^"]+)"""
  ]


}
```