#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-user-privilege-use-success-4673-1
  Vendor = Microsoft
  Product = Event Viewer - Security
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ "__li_source_path=", "A privileged service was called","""eventid="4673"""" ]
  Fields = [
    """({event_name}A privileged service was called)""",
    """__li_source_path="({host}[^"]+)"""",
    """__li_source_path="({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""",
    """({event_code}4673)""",
    """(K|k)eywords="({result}[^"]+)"""",
    """Process Name:\s+(?: |({process_path}({process_dir}(?:[^"]+)?[\\\/])?({process_name}[^\\\/"]+?)))\s+Service""",
    """\s+Account Domain:\s+({domain}.+?)\s+Logon ID:\s+({login_id}[^\s]+)""",
    """(?:Information|Success Audit|Audit Success).+?Account Name:\s+({user}.+?)\s+Account Domain:""",
    """Server:\s+({object_server}.+?)\s+Service Name""",
    """Privileges:\s+({privileges}.+?)(,\d+|\s*$)""",
    """\s+({ownership_privilege}SeTakeOwnershipPrivilege)""",
    """\s+({environment_privilege}SeSystemEnvironmentPrivilege)""",
    """\s+({debug_privilege}SeDebugPrivilege)""",
    """\s+({tcb_privilege}SeTcbPrivilege)"""
  ]


}
```