#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-share-modify-success-5143
  Vendor = Microsoft
  Product = Event Viewer - Security
  ParserVersion = "v1.0.0"
  TimeFormat = "EEE MMM dd HH:mm:ss yyyy"
  Conditions = [ """5143""", """A network share object was modified.""", """MSWinEventLog""", """Microsoft-Windows-Security-Auditing""" ]
  Fields = [
    """({time}\w+\s+\w+\s+\d+\s+\d+:\d+:\d+\s+\d+)\s+({event_code}\d+)\s+Microsoft-Windows-Security-Auditing""",
    """\d\d:\d\d:\d\d\s+({host}[\w\-.]+)\s+MSWinEventLog""",
    """Microsoft-Windows-Security-Auditing\s+\S+\s+\S+\s+({result}[^\s]+\sAudit)""",
    """({event_name}A network share object was modified)""",
    """Subject:\s+Security ID:\s+({user_sid}[^\s]+)""",
    """Account Name:\s+({user}[\w\.\-]{1,40}\$?)""",
    """Account Domain:\s+({domain}[^\s]+)""",
    """Logon ID:\s+({login_id}[^\s]+)""",
    """Share Information:\s+Object Type:\s+({file_type}[^:]+?)\s+Share Name:""",
    """Share Name:\s+[\\\*]*({share_name}[^\s]+)\s+Share Path:""",
    """Share Path:\s*[\\\?]*({share_path}(({d_parent}[^@]+?)\\)?(|({d_name}[^\\]+?)))\s*Old Remark:"""
  ]


}
```