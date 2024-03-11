#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-user-privilege-success-467
    Vendor = Microsoft
    Product = Event Viewer - Security
    ParserVersion = "v1.0.0"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Conditions = ["""LogType="WLS"""", """EventID="467"""]
    Fields = [
      """Computer="+({host}[^".]+)""",
      """"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
      """EventID="+({event_code}[^"]+)"""",
      """Keywords="+({result}[^"]+)"""",
      """SubjectUserName ="+({user}[^"]+)"""",
      """SubjectDomainName ="+({domain}[^"]+)"""",
      """SubjectLogonId="+({login_id}[^"]+)"""",
      """ProcessName ="+(?: |({process_path}({process_dir}(?:[^"]+)?[\\\/])?({process_name}[^"]+)))"+,""",
      """PrivilegeList="+({privileges}[^"]+)"""",
      """AccessMask="+({access}[^"]+)"""",
      """ObjectName ="+(?:-|({object}[^"]+))"""",
      """ObjectType="+(?:-|({object_type}[^"]+))"""",
      """ObjectServer="+(?:-|({object_server}[^"]+))""""
    ]
    DupFields = ["host->dest_host","directory->process_dir"]
  

}
```