#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-share-access-success-5143
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security 
  TimeFormat = "MM/dd/yyyy HH:mm:ss a"
  Conditions = [ """EventCode=5143""", """A network share object was modified.""", """ComputerName =""", """SourceName =Microsoft Windows security auditing""" ]
  Fields = [
    """({time}\d\d\/\d\d\/\d\d\d\d \d\d:\d\d:\d\d \w\w)""",
    """({event_code}5143)""",
    """ComputerName =({host}[\w\-\.]+)""",
    """({event_name}A network share object was modified)""",
    """Keywords=({result}[^=]+?)\s*\w+=""",
    """Subject:\s+Security ID:\s+({user_sid}[^\s]+)""",
    """Account Name:\s+({user}[^\s]+)""",
    """Account Domain:\s+({domain}[^\s]+)""",
    """Logon ID:\s+({login_id}[^\s]+)""",
    """Share Information:\s+Object Type:\s+({file_type}[^:]+?)\s+Share Name:""",
    """Share Name:\s+[\\\*]*({share_name}[^\s]+)\s+Share Path:""",
    """Share Path:\s*[\\\?]*({share_path}(({d_parent}[^@]+?)\\)?(|({d_name}[^\\]+?)))\s*Old Remark:"""
    """Source Port(=|:)\s*({src_port}\d+)"""
  ]


}
```