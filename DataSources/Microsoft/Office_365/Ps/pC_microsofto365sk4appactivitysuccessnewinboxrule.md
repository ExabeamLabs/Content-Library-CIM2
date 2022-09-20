#### Parser Content
```Java
{
Name = microsoft-o365-sk4-app-activity-success-newinboxrule
  Vendor = Microsoft
  Product = Office 365
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = ["""New-InboxRule""" ]
  Fields = [
    """time="({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
    """host="({host}[^"]+)"""",
    """"CreationTime":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""",
    """"Name":"ForwardTo".+?"Value":"(?:smtp:)?({target}[^"]+)""""
    """"ResultStatus":"({result}[^"]+)"""",
    """"ClientIP":"({src_ip}[^:]+):""",
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