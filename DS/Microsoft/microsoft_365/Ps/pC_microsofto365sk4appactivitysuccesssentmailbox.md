#### Parser Content
```Java
{
Name = microsoft-o365-sk4-app-activity-success-sentmailbox
  Vendor = Microsoft
  Product = Microsoft 365
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = ["""Operation":"Set-Mailbox""" ]
  Fields = [
    """"TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)Z"""",
    """"CreationTime":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""",
    """Forward[^\}]+?Value":"(smtp:)?({target}[^"]+@({dest_domain}[^"]+))""""
    """"ResultStatus":"({result}[^"]+)"""",
    """"ClientIP":"\[?({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """({operation}Set-Mailbox)""",
    """Operation":"({operation}[^"]+)"""",
    """cs1=(\[\{"additional-properties"\:)?\{"({policy_name}[^"]+)""",
    """msg=({additional_info}[^=]+?)\s\w+=""",
    """"Value":"(?:smtp:)?[^@]+?@({dest_domain}[^;"]+)"""",
    """UserId":"({email_address}[^"\\\s@]+@({email_domain}[^"\\\s@]+\.[^"\\\s@]+))""",
    """destinationServiceName =({app}[^=]+?)\s*filePath"""
    """({app}Office 365)"""
  ]
  DupFields = ["domain->email_domain"]


}
```