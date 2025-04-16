#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-file-read-success-4663
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss", "MMM dd HH:mm:ss"]
  Conditions = [ """LogType="WLS"""", """EventID="4663"""" ]
  Fields = [
    """({time}\w+\s+\d+ \d+:\d+:\d+)"""
    """({event_name}An attempt was made to access an object)""",
    """Computer="+({host}[^"]+)"""",
    """"({time}\d\d\d\d\-\d+\-\d+T\d\d:\d\d:\d\d)""",
    """EventID="+({event_code}[^"]+)"""",
    """EventRecordID="+({event_id}[^"]+)"""",
    """SubjectUserName ="+({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""",
    """SubjectUserSid="+({user_sid}[^"]+)"""",
    """SubjectDomainName ="+({domain}[^"]+)"""",
    """SubjectLogonId="+({login_id}[^"]+)"""",
    """ObjectType="+({file_type}[^"]+)""",
    """ObjectName ="+(({registry_path}\\+REGISTRY[^"]+?(\\\{({registry_key}[^\}"]+)\})?)|({src_file_path}[^"]+))""",
    """ObjectName ="+(?!\\+REGISTRY).*\\({src_file_name}(?:[^\\:]+(?=\.))({src_file_ext}\.[^\\:]+)?|[^\\:]+)"+,\s*ObjectServer=""",
    """ObjectName ="+(?!\\+REGISTRY)(?:({file_dir}.+?)\\+[^\\]+)",""",
    """ProcessName ="+({process_path}({process_dir}(?:[^"]+)?[\\\/])?({process_name}[^\\\/"]+))"""",
    """AccessList="({access}[^"]+)""",
    """AccessMask="({access_mask}[^"]+)"""
  ]
  DupFields = [ "host->src_host", "user->src_user", "domain->src_domain" ]
  ParserVersion = "v1.0.0"


}
```