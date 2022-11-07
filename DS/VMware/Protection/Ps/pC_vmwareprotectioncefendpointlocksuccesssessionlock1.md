#### Parser Content
```Java
{
Name = vmware-protection-cef-endpoint-lock-success-sessionlock-1
Vendor = "VMware"
Product = "Protection"
TimeFormat = "epoch"
Conditions = [
  """CEF:"""
  """|Carbon Black|App Control|"""
  """Event[00000007] Type[SessionLock]"""
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