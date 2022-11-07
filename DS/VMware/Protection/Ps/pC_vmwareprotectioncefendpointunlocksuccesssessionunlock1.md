#### Parser Content
```Java
{
Name = vmware-protection-cef-endpoint-unlock-success-sessionunlock-1
Vendor = "VMware"
Product = "Protection"
TimeFormat = "epoch"
Conditions = [
  """|Carbon Black|App Control|"""
  """Event[00000008] Type[SessionUnlock]"""
]
Fields = [
  """\Wrt=({time}\d+)"""
  """\Wdvc=({host_ip}[a-fA-F:\d.]+)"""
  """\Wdvchost=({host}[\w\-.]+)"""
  """\Wdhost=(({domain}[^\\]+)\\+)?({dest_host}[^\\\s]+)"""
  """\Wdst=({dest_ip}[a-fA-F:\d.]+)"""
  """\Wduser=(({domain}[^\\]+)\\+)?({user}[^\\\s]+)"""
  """\WEvent\[({event_code}\d+)\]\s*Type\[Session"""
]
ParserVersion = "v1.0.0"


}
```