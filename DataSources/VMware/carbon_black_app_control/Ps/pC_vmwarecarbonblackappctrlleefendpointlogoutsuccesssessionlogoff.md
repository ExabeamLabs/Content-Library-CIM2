#### Parser Content
```Java
{
Name = vmware-carbonblackappctrl-leef-endpoint-logout-success-sessionlogoff
  ParserVersion = "v1.0.0"
  Conditions = [ """LEEF:""", """|Carbon_Black|Protection|""", """Event[00000006] Type[SessionLogoff]""" ]

leef-carbonblack-events-1 = {
  Vendor = VMware
  Product = carbon black app control
  TimeFormat = "MMM dd yyyy HH:mm:ss.SSS z"
  Fields = [
    """({host}[\w\-.]+)\s+LEEF:""",
    """\WdevTime=({time}\w+\s+\d+\s+\d\d\d\d\s+\d\d:\d\d:\d\d\.\d+ \w+)""",
    """\Wsrc=({src_ip}[A-Fa-f:\d.]+)""",
    """\WsrcHostName =(({domain}[^\\\s]+)\\+)?({src_host}[\w\-.]+)""",
    """\WdstHostName =({dest_host}[\w\-.]+)""",
    """\WEvent\[({event_code}\d+)\]\s*Type\[""",
    """\WUser\[(({domain}[^\\\s\]]+)\\+)?(|({user}[^\\\s\]]+))\]""",
  
}
```