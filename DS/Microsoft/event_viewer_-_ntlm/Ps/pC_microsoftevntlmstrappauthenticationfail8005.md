#### Parser Content
```Java
{
Name = microsoft-evntlm-str-app-authentication-fail-8005
  Vendor = Microsoft
  Product = Event Viewer - NTLM
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """ (8005) """, """security policy Network Security:""", """Restrict NTLM:""" ]
  Fields = [
    """({time}\d+-\d+-\d+T\d+:\d+:\d+)\S*\s+({host}[\w\-.]+)\s+EvntSLog""",
    """({event_code}8005)""",
    """Channel name:\s*({resource}.*?)\s+User name:""",
    """User name:\s*(NULL|({user}[\w\.\-]{1,40}\$?))\s+Domain name:""",
    """Domain name:\s*(NULL|({domain}[^\s\(\)]*?))\s+Workstation name:""",
    """Workstation name:\s*\\?(NULL|({src_host}[\w\-.]+))\s+Secure Channel type:""",
# channel_type is removed
    """security policy Network Security:\s*Restrict NTLM:\s*({policy_name}[^\.]+)""",
  ]


}
```