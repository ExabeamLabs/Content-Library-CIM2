#### Parser Content
```Java
{
Name = vmware-esxi-str-http-close-6876
  ParserVersion = v1.0.0
  Vendor = VMware
  Product = VMware ESXi
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """Originator@6876""", """] [""", """sub=""", """The client closed the stream, not unexpectedly.""" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d+Z)\s+({host}[^\s]+)\s[^:]+:\s+({additional_info}[^"]+?)\s*$""",
    """user=((({domain}[^\\\s@]+)\\+)?({user}[\w\.\-]{1,40}\$?))"""
  ]


}
```