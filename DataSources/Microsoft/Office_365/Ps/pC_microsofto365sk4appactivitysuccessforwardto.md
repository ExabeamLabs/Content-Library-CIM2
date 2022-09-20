#### Parser Content
```Java
{
Name = microsoft-o365-sk4-app-activity-success-forwardto
  Vendor = Microsoft
  Product = Office 365
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = ["""New-InboxRule""" , """ForwardTo""" ]
  Fields = [
    """"CreationTime":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""",
    """Forward.+?Value":"(smtp:)?({target}[^"]+@({dest_domain}[^"]+))""""
    """"ResultStatus":"({result}[^"]+)"""",
    """"ClientIP":"({src_ip}[^:]+):""",
    """({operation}ForwardTo)"""",
    """msg=({additional_info}.+?)\srequest=""",
    """UserId":"({email_address}[^"\\]+@({domain}[^"]+))""",
    """destinationServiceName =({app}.+?)\s(device|filePath)""",
    """({app}Office 365)"""
    """"SubjectOrBodyContainsWords":"({filter_key_words}[^"]+)"""
  ]
  DupFields = ["domain->email_domain"]


}
```