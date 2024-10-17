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
    """\Wsrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\WsrcHostName =(({domain}[^\\\s]+)\\+)?({src_host}[\w\-.]+)""",
    """\WdstHostName =({dest_host}[\w\-.]+)""",
    """\WEvent\[({event_code}\d+)\]\s*Type\[""",
    """\WUser\[(({domain}[^\\\s\]]+)\\+)?(|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\]""",
  ]
  ParserVersion = "v1.0.0"


}
```