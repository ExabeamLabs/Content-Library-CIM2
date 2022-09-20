#### Parser Content
```Java
{
Name = vmware-carbonblackappctrl-leef-endpoint-login-success-protection
  Vendor = VMware
  Product = Carbon Black App Control
  TimeFormat = "MMM dd yyyy HH:mm:ss.SSS z"
  Conditions = [ """LEEF:""", """|Carbon_Black|Protection|""", """Event[00000005] Type[SessionLogon]""" ]
  Fields = [
    """({host}[\w\-.]+)\s+LEEF:""",
    """\WdevTime=({time}\w+\s+\d+\s+\d\d\d\d\s+\d\d:\d\d:\d\d\.\d+ \w+)""",
    """\Wsrc=({src_ip}[A-Fa-f:\d.]+)""",
    """\WsrcHostName =(({domain}[^\\\s]+)\\+)?({src_host}[\w\-.]+)""",
    """\WdstHostName =({dest_host}[\w\-.]+)""",
    """\WEvent\[({event_code}\d+)\]\s*Type\[""",
    """\WUser\[(({domain}[^\\\s\]]+)\\+)?(|({user}[^\\\s\]]+))\]""",
  ]
  ParserVersion = "v1.0.0"


}
```