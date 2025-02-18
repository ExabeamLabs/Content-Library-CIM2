#### Parser Content
```Java
{
Name = microsoft-o365-json-app-activity-success-updateinboxrules
  ExtractionType = json
  Vendor = Microsoft
  Product = Microsoft 365
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss", "yyyy-MM-dd'T'HH:mm:ssZ"]
  Conditions = [""""UpdateInboxRules"""" ,""""Forward""", """"ClientRequestId":""", """"MailboxGuid":""" ]
  Fields = [
    """"OriginatingServer":\s*"({host}[\w\-.]+)\s""",
    """"CreationTime":\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """"ResultStatus":\s*"({result}[^"]+)"""",
    """"ClientIP":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"UserId":\s*"({email_address}[^@"]+@({domain}[^"]+))"""",
    """"ActionType(\\)?":(\\)?"({operation}[^"\\]+)(\\)?"""",
    """"Operation":\s*"({event_name}[^"]+)"""",
    """Forward[^\}\]]+Recipients(\\)?":\[[\\"]*({recipients}({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|\\]+))[^\]]*?)[\\"]*\]"""
    """"Workload":\s*"({app}[^"]+)"""",
    """"UserType":\s*"*({user_type}[^\}"]+)\s*"*(,|\})"""
    """"ClientProcessName":\s*"({process_name}[^"]+)""""
    """exa_json_path=$..OriginatingServer,exa_regex=({host}[\w\-.]+)"""
    """exa_json_path=$..CreationTime,exa_field_name=time"""
    """exa_json_path=$..ResultStatus,exa_field_name=result"""
    """exa_json_path=$..ClientIP,exa_field_name=src_ip"""
    """exa_json_path=$..UserId,exa_regex=({email_address}[^@"]+@({domain}[^"]+))"""
    """exa_regex="ActionType(\\)?":(\\)?"({operation}[^"\\]+)(\\)?""""
    """exa_json_path=$..Operation,exa_field_name=event_name"""
    """exa_json_path=$..OperationProperties,exa_regex=Forward[^\}\]]+Recipients(\\)?":\[(\\)?({recipients}"({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))[^\]]+)\]""",
    """exa_json_path=$..Workload,exa_field_name=app"""
    """exa_json_path=$..ClientProcessName,exa_field_name=process_name"""
    """exa_regex="UserType":\s*"*({user_type}[^\}"]+)\s*"*(,|\})"""
  ]
  DupFields = [ "dest_email_address->target" ]
  ParserVersion = "v1.0.0"


}
```