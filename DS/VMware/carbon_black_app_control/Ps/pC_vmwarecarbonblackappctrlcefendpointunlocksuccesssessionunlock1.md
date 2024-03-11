#### Parser Content
```Java
{
Name = vmware-carbonblackappctrl-cef-endpoint-unlock-success-sessionunlock-1
Vendor = "VMware"
Product = "Carbon Black App Control"
TimeFormat = "epoch"
Conditions = [
  """|Carbon Black|App Control|"""
  """Event[00000008] Type[SessionUnlock]"""
]
Fields = [
  """\Wrt=({time}\d{13})"""
  """\Wdvc=({host_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
  """\Wdvchost=({host}[\w\-.]+)"""
  """\Wdhost=(({domain}[^\\]+)\\+)?({dest_host}[^\\\s]+)"""
  """\Wdst=({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """\Wduser=(({domain}[^\\]+)\\+)?({user}[^\\\s]+)"""
  """\WEvent\[({event_code}\d+)\]\s*Type\[Session"""
]
ParserVersion = "v1.0.0"


}
```