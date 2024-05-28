#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-file-read-success-4663-4
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """Microsoft-Windows-Security-Auditing """, """EventID="4663"""", """An attempt was made to access an object""" ]
  Fields = [
    """({event_name}An attempt was made to access an object)""",
    """Computer="+({host}[^"]+)"""",
    """({time}\d\d\d\d\-\d+\-\d+T\d\d:\d\d:\d\d)""",
    """EventID="+({event_code}[^"]+)"""",
    """SubjectUserName ="+({user}[\w\.\-]{1,40}\$?)"""",
    """SubjectUserSid="+({user_sid}[^"]+)"""",
    """SubjectDomainName ="+({domain}[^"]+)"""",
    """SubjectLogonId="+({login_id}[^"]+)"""",
    """Category="+({category}[^"]+)""",
    """ObjectType="+({file_type}[^"]+)""",
    """ObjectName ="+({src_file_path}[^"]+)""",
    """ObjectName ="+.*\\({src_file_name}(?:[^\\:]+(?=\.))({src_file_ext}\.[^\\:]+)?|[^\\:]+)"+,\s*ObjectServer=""",
    """ObjectName ="+(?:({file_dir}.+?)\\+[^\\]+)",""",
    """ProcessName ="+({process_path}({process_dir}(?:[^"]+)?[\\\/])?({process_name}[^\\\/"]+))"""",
    """AccessList="({access}[^"]+)""",
    """AccessMask="({access_mask}[^"]+)""",
    """Accesses:\s*({additional_info}.+?)\s+Access Mask:"""
  ]
  DupFields = [ "host->src_host" ]
  ParserVersion = "v1.0.0"


}
```