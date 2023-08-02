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
    """Security ID:\s*(?!NT AUTHORITY)(({account_domain}[^\\\/:]+?)[\\\/]+)?({account}[^\s:]+?)(?<!SYSTEM)\s+"""
    """Account Name:\s*({user}\S+)\s+Account Domain:""",
    """Account Domain:\s*({domain}\S+)\s+Logon ID:""",
    """Logon ID:\s*({login_id}\S+)\s+Object:""",
    """Object Server:\s*({object_server}\S.*?)\s+Object Type:""",
    """Object Type:\s*({object_type}\S+)\s*Object Name:""",
    """Object Name:\s*({object}\S.*?)\s*Handle ID:""",
    """Handle ID:\s*({handle_id}\S+)""",
    """Process ID:\s*({process_id}[^\s]*)""",
    """Process Name:\s*({process_path}({process_dir}.+)[\\\/]({process_name}.+?))\s*Auditing Settings:""",
  ]


}
```