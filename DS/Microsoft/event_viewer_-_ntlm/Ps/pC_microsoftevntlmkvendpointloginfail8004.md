#### Parser Content
```Java
{
Name = microsoft-evntlm-kv-endpoint-login-fail-8004
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - NTLM
  TimeFormat = "MM/dd/yyyy HH:mm:ss"
  Conditions = [ """security policy Network Security:""", """Restrict NTLM:""", """EventCode=8004""" ]
  Fields = [
    """({event_name}Domain Controller Blocked Audit: Audit NTLM authentication to this domain controller)""",
    """({time}\d\d/\d\d/\d\d\d\d \d\d:\d\d:\d\d)""",
    """ComputerName =({host}[^\s]+)""",
    """({event_code}8004)""",
    """User name:\s+({user}[^\s]+)""",
    """Domain name:\s+(NULL|({domain}[^\s]+))""",
    """RecordNumber=({event_id}\d+)""",
    """Channel name:\s*({resource}.*?)\s+User name:""",
    """Workstation name:\s*\\?(NULL|({src_host}[\w\-.]+))\s+Secure Channel type:""",
    """security policy Network Security:\s*Restrict NTLM:\s*({policy_name}[^\.]+)""",
  ]
  DupFields = ["host->dest_host"]


}
```