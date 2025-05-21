#### Parser Content
```Java
{
Name = vmware-carbonblackappctrl-cef-endpoint-login-success-00000005
  Vendor = VMware
  Product = Carbon Black App Control
  TimeFormat = "epoch"
  Conditions = [ """|Carbon Black|App Control|""", """Event[00000005] Type[SessionLogon]""" ]
  Fields = [
    """\Wrt=({time}\d{13})""",
    """\Wdvc=({host_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""",
    """\Wdvchost=({host}[\w\-.]+)""",
    """\Wdhost=(({domain}[^\\]+)\\+)?({dest_host}[^\\\s]+)""",
    """\Wdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """\Wduser=(({domain}[^\\]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
    """\WEvent\[({event_code}\d+)\]\s*Type\[Session"""
  ]
  ParserVersion = "v1.0.0"


}
```