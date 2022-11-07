#### Parser Content
```Java
{
Name = microsoft-o365-sk4-app-activity-success-forward
  Vendor = Microsoft
  Product = Office 365
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [""""UpdateInboxRules"""" , """"ActionType":"Forward"""","""destinationServiceName =""" ]
  Fields = [
    """"CreationTime":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """"ResultStatus":"({result}[^"]+)"""",
    """"ClientIP":"(\[)?({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})(\])?(:({src_port}\d+))?""",
    """UserId":"({email_address}[^"\\]+@({domain}[^"]+))""",
    """"ActionType":"({operation}[^"]+)"""",
    """destinationServiceName =({app}[^=]+?)\s+\w+=""",
    """"SubjectOrBodyContainsWords":"({filter_key_words}[^"]+)""",
    """flexString1=({event_name}[^=]+?)\s+\w+=""",
    """Forward.+?Recipients\\?":\[?\\?"({target}[^\@]+@({dest_domain}[^",;\\]+))"""
  ]
  DupFields = ["domain->email_domain"]


}
```