#### Parser Content
```Java
{
Name = vmware-carbonblackappctrl-leef-endpoint-lock-success-sessionlock
  Conditions = [ """LEEF:""", """|Carbon_Black|Protection|""", """Event[00000007] Type[SessionLock]""" ]
  ParserVersion = "v1.0.0"

leef-carbonblack-events = {
  Vendor = VMware
  Product = Carbon Black App Control
  TimeFormat = "MMM dd yyyy HH:mm:ss.SSS z"
  Fields = [
    """({host}[\w\-.]+)\s+LEEF:""",
    """\WdevTime=({time}\w+\s+\d+\s+\d\d\d\d\s+\d\d:\d\d:\d\d\.\d+ \w+)""",
    """\Wsrc=({src_ip}[A-Fa-f:\d.]+)""",
    """\WsrcHostName =(({domain}[^\\\s]+)\\+)?({src_host}[\w\-.]+)""",
    """\WdstHostName =({src_host}[\w\-.]+)""",
    """\WEvent\[({event_code}\d+)\]\s*Type\[""",
    """\WUser\[(({domain}[^\\\s\]]+)\\+)?(|({user}[^\\\s\]]+))\]""",
  
}
```