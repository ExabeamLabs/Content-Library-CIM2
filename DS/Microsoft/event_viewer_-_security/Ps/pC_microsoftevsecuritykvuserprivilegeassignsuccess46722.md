#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-user-privilege-assign-success-4672-2
  Vendor = Microsoft
  Product = Event Viewer - Security 
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ "__li_source_path=", "Special privileges assigned to new logon","""eventid="4672"""" ]
  Fields = [
    """({event_name}Special privileges assigned to new logon)""",
    """__li_source_path="({host}[^"]+)"""",
    """__li_source_path="({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""",
    """({event_code}4672)""",
    """(K|k)eywords="({result}[^"]+)"""",
    """(?:Information|Success Audit|Audit Success).+?Account Name:\s+({user}.+?)\s+Account Domain""",
    """\s+Account Domain:\s+({domain}[^\s]+)""",
    """\s+Logon ID:\s+({login_id}[^\s]+)""",
    """\s+Privileges:\s+({privileges}.+?)(,\d+|\s*$)""",
    """\s+({ownership_privilege}SeTakeOwnershipPrivilege)""",
    """\s+({environment_privilege}SeSystemEnvironmentPrivilege)""",
    """\s+({debug_privilege}SeDebugPrivilege)""",
    """\s+({tcb_privilege}SeTcbPrivilege)"""
  ]


}
```