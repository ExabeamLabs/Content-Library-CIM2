#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-file-fileoperation
  Vendor = Microsoft
  Product = Event Viewer - Security
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """Key file operation.""", """Key Type:""", """Key File Operation Information:""", """Return Code:""" ]
  Fields = [
    """({event_name}Key file operation)""",
    """Account Name:\s+({user}[^\s]+)\s+Account Domain:""",
    """Account Domain:\s+({domain}[^\s]+)\s+Logon ID:""",
    """Logon ID:\s+({login_id}[^\s]+)\s+\w+""",
    """Operation:\s+({operation}[^$]+?)\s+Return Code:"""
  ]


}
```