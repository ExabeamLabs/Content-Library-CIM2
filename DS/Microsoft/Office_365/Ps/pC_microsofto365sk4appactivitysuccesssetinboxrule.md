#### Parser Content
```Java
{
Name = microsoft-o365-sk4-app-activity-success-setinboxrule
  Vendor = Microsoft
  Product = Office 365
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = ["""Operation":"Set-InboxRule""" ]
  Fields = [
    """"CreationTime":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""",
    """Forward.+?Value":"(smtp:)?({target}[^"]+@({dest_domain}[^"]+))""""
    """"ResultStatus":"({result}[^"]+)"""",
    """"ClientIP":"({src_ip}[^:]+):""",
    """({operation}Set-Mailbox)""",
    """cs1=(\[\{"additional-properties"\:)?\{"({operation}[^"]+)""",
    """msg=({additional_info}.+?)\s\w+=""",
    """"Value":"(?:smtp:)?.+?@({dest_domain}[^"]+)"""",
    """UserId":"({email_address}[^"\\]+@({domain}[^"]+)[^"]+)"""",
    """UserId":"(\\.+)?\/({full_name}[^,\\"]+)\\"\s*on behalf""",
    """UserId":"(\\.+)?\/({last_name}[^,]+),\s*({first_name}[^\\"]+)\\"\s*on behalf""",
    """UserId":"({email_address}[^"\\]+@({domain}[^"]+)[^"]+)"""",
    """destinationServiceName =({app}.+?)\s*filePath"""
    """({app}Office 365)"""
    """"SubjectOrBodyContainsWords":"({filter_key_words}[^"]+)"""
  ]
  DupFields = ["domain->email_domain"]


}
```