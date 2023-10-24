#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-audit-policy-modify-4907
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "MMM dd HH:mm:ss yyyy"
  Conditions = [ """4907""", """Auditing settings on object were changed""" ]
  Fields = [
    """({time}\d+-\d+-\d+T\d+:\d+:\d+)\S*\s+({host}[\w\-.]+)\s+EvntSLog""",
    """(Mon|Tue|Wed|Thu|Fri|Sat|Sun) ({time}\w+ \d+ \d+:\d+:\d+ \d+)"""
    """({event_code}4907)""",
    """({event_name}Auditing settings on object were changed)""",
    """Security ID:\s*(?!NT AUTHORITY)(({account_domain}[^\\\/:]+?)[\\\/]+)?(\\t|\\n|\\r)*({account}[^\\\s:]+)(?<!SYSTEM)\s*"""
    """Account Name:\s*({user}[\w\.\-]{1,40}\$?)\s+Account Domain:""",
    """Account Domain:\s*({domain}\S+)\s+Logon ID:""",
    """Logon ID:\s*({login_id}\S+)\s+Object:""",
    """Object Server:\s*({object_server}\S.*?)\s+Object Type:""",
    """Object Type:\s*(\\t|\\n|\\r)*({object_type}[^\\\s]+)\s*(\\t|\\n|\\r)*Object Name:""",
    """Object Name:\s*(\\t|\\n|\\r)*({object}\S.*?)\s*(\\t|\\n|\\r)*Handle ID:""",
    """Handle ID:\s*(\\t|\\n|\\r)*({handle_id}[^\\\s]+)\s*(\\t|\\n|\\r)*""",
    """Process ID:\s*(\\t|\\n|\\r)*({process_id}[^\\\s]+)\s*(\\t|\\n|\\r)*""",
    """Process Name:\s*((\\)*(\\r|\\t|\\n))*({process_path}({process_dir}[^=]*?)(\\+({process_name}[^\\]+?))?)((\\)*(\\r|\\t|\\n))*\s*Auditing Settings:""",
  ]


}
```