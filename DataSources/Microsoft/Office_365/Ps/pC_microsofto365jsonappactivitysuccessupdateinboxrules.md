#### Parser Content
```Java
{
Name = microsoft-o365-json-app-activity-success-updateinboxrules
  Vendor = Microsoft
  Product = Office 365
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [""""UpdateInboxRules"""" ,""""Forward""", """"ClientRequestId":""", """"MailboxGuid":""" ]
  Fields = [
    """"OriginatingServer":\s*"({host}[\w\-.]+)\s""",
    """"CreationTime":\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """"ResultStatus":\s*"({result}[^"]+)"""",
    """"ClientIP":\s*"({src_ip}[A-Fa-f\d:.]+)"""",
    """"UserId":\s*"({email_address}[^@"]+@({domain}[^"]+))"""",
    """"ActionType(\\)?":(\\)?"({operation}[^"\\]+)(\\)?"""",
    """"Operation":\s*"({event_name}[^"]+)"""",
    """Forward[^\}\]]+Recipients(\\)?":\[(\\)?({recipients}"({recipient}[^\\",;@]+@({dest_domain}[^\\",;@]+))[^\]]+)\]""",
    """"Workload":\s*"({app}[^"]+)"""",
    """"ClientProcessName":\s*"({process_name}[^"]+)""""
  ]
  DupFields = [ "recipient->target" ]
  ParserVersion = "v1.0.0"


}
```