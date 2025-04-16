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
      """Computer="+({host}[\w\-.]+)""",
      """"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
      """EventID="+({event_code}[^"]+)"""",
      """Keywords="+({result}[^"]+)"""",
      """SubjectUserName ="+({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""",
      """SubjectDomainName ="+({domain}[^"]+)"""",
      """SubjectLogonId="+({login_id}[^"]+)"""",
      """ProcessName ="+(?: |({process_path}({process_dir}(?:[^"]+)?[\\\/])?({process_name}[^"]+)))"+,""",
      """PrivilegeList="+({privileges}[^"]+)"""",
      """AccessMask="+({access}[^"]+)"""",
      """ObjectName ="+(?:-|({object}[^"]+))"""",
      """ObjectType="+(?:-|({object_type}[^"]+))"""",
      """ObjectServer="+(?:-|({object_server}[^"]+))""""
    ]
    DupFields = ["host->dest_host","directory->process_dir","user->src_user", "domain->src_domain"]
  

}
```