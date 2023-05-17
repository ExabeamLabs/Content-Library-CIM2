#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-handle-request-4659
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
  Conditions = ["""A handle to an object was requested with intent to delete""", """>4659<""", """Microsoft-Windows-Security-Auditing"""]
  Fields = [
    """({event_name}A handle to an object was requested with intent to delete)""",
    """({event_code}4659)""",
    """>\s({host}\w+)\s<""",
    """Handle ID:\s+({object_id}[^\s]+)\s+Process Information:""",
# process_info is removed
    """Transaction ID:\s+({transaction_id}[^\s]+)\s+Accesses:""",
    """<TimeCreated SystemTime\\*='({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)""",
    """<Computer>({dest_host}({host}[^<>]+))<\/Computer>""",
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
    """ThreadID\\*='({thread_id}\d+)'""",
    """<Keyword>({result}[^<]+)<""",
    """<Task>({operation}File System)"""
    """<Provider>({provider_name}[^<]+)"""
    """Security ID:\s*({user_sid}\S+)\s+"""
    """Account Name:\s*({user}\S+)\s+"""
    """Account Domain:\s*({domain}\S+)\s+"""
    """Logon ID:\s*({login_id}\S+)\s+"""
    """Object Server:\s*({object_server}\S.*?)\s+"""
    """Object Type:\s*({object_type}\S+)\s*"""
    """Object Name:\s*({object}\S.+?)\s+"""
    """Accesses:\s*(-|({access}[^\s]+))\s*"""
    """Process ID:\s*({process_id}\S+)\s+"""
  ]


}
```