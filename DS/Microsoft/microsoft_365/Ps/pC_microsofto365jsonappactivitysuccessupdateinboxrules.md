#### Parser Content
```Java
{
Name = microsoft-o365-json-app-activity-success-updateinboxrules
  Vendor = Microsoft
  Product = Microsoft 365
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [""""UpdateInboxRules"""" ,""""Forward""", """"ClientRequestId":""", """"MailboxGuid":""" ]
  Fields = [
    """"OriginatingServer":\s*"({host}[\w\-.]+)\s""",
    """"CreationTime":\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """"ResultStatus":\s*"({result}[^"]+)"""",
    """"ClientIP":\s*"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"UserId":\s*"({email_address}[^@"]+@({domain}[^"]+))"""",
    """"ActionType(\\)?":(\\)?"({operation}[^"\\]+)(\\)?"""",
    """"Operation":\s*"({event_name}[^"]+)"""",
    """Forward[^\}\]]+Recipients(\\)?":\[(\\)?({recipients}"({dest_email_address}[^\\",;@]+@({dest_domain}[^\\",;@]+))[^\]]+)\]""",
    """"Workload":\s*"({app}[^"]+)"""",
    """"ClientProcessName":\s*"({process_name}[^"]+)""""
  ]
  DupFields = [ "dest_email_address->target" ]
  ParserVersion = "v1.0.0"


}
```