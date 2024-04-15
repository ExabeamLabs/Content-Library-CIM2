#### Parser Content
```Java
{
Name = "vmware-carbonblackappctrl-cef-endpoint-login-success-000000005"
  ParserVersion = "v1.0.0"
  Vendor = "VMware"
  Product = "Carbon Black App Control"
  TimeFormat = "epoch"
  Conditions = [ """|Carbon Black|Protection|""", """Event[00000005] Type[SessionLogon]""" ]
  Fields = [
    """\Wrt=({time}\d{13})""",
    """\Wdvc=({host}[a-fA-F:\d.]+)""",
    """\Wdvchost=({host}[\w\-.]+)""",
    """\Wdhost=(({domain}[^\\\/=]+)[\\\/]+)?({dest_host}[^\s=]+)""",
    """\Wdst=({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """\Wduser=(({domain}[^\\\/=]+)[\\\/]+)?({user}[^\s=]+)""",
    """\WEvent\[({event_code}\d+)\]\s*Type\[Session"""
  ]


}
```