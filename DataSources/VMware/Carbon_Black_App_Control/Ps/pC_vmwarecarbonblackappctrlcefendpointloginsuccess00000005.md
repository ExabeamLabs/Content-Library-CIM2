#### Parser Content
```Java
{
Name = vmware-carbonblackappctrl-cef-endpoint-login-success-00000005
  Vendor = VMware
  Product = Carbon Black App Control
  TimeFormat = "epoch"
  Conditions = [ """|Carbon Black|App Control|""", """Event[00000005] Type[SessionLogon]""" ]
  Fields = [
    """\Wrt=({time}\d+)""",
    """\Wdvc=({host_ip}[a-fA-F:\d.]+)""",
    """\Wdvchost=({host}[\w\-.]+)""",
    """\Wdhost=(({domain}[^\\]+)\\+)?({dest_host}[^\\\s]+)""",
    """\Wdst=({dest_ip}[a-fA-F:\d.]+)""",
    """\Wduser=(({domain}[^\\]+)\\+)?({user}[^\\\s]+)""",
    """\WEvent\[({event_code}\d+)\]\s*Type\[Session"""
  ]
  ParserVersion = "v1.0.0"


}
```